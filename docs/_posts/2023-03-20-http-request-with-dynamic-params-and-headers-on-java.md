# Http request with dynamic parameters and headers in Java (using okHttp)

 
<p><img src="/assets/images/hal-gatewood-tZc3vjPCk-Q-unsplash.jpg" alt="Sketch of three webpages" width="400"></p>

As a new joiner in my company, I have been asked to do a little Java/Spring/Maven project based around making calls to an external API. Until now, I had never used Java, so although I knew the basics of what I had to do, it was all fairly new to me.

 

It’s been a lot of trial an error, I have looked everywhere in the internet trying to find what I was looking for without much success, having to take small bits here and there to try to achieve what I had in mind. That’s why I decided to write down that little adventure so that, hopefully, this will make it a bit easier if someone else (or maybe even a future me) is looking for something similar.

 

On this post, I will show you how to create a request with dynamic parameters and headers, as well as parsing a simple response to extract the information you need. 

 

This would be a typical okHttp request with hardcoded headers and params:

 

```

public void loginToAPI(username, password)
      throws Exception{
        RequestBody formBody = new FormBody.Builder()
                .add("username", username)
                .add("password", password)
                .build();

        Request request = new Request.Builder()
                .url(this.URL)
                .addHeader("Content-Type", "application/x-www-form-urlencoded")
                .addHeader("Accept", "application/json")
                .post(formBody)
                .build();

        Response response = client.newCall(request).execute();

        if (!response.isSuccessful()){
            throw new IOException("Unexpected code " + response);
        }
    }

```

In this case, we have a POST request, for the GET request you don’t need to indicate the method as it is the default. You can also use PUT and DELETE.

In the following code, I have created a method that allows you to set dynamic parameters and dynamic headers using a HashMap containing the keys and values for both, as well as the method and URL that your request will be using. This is quite a handy class to be extended and cover most of the functionality you will need in your application when consuming an API.

 

```

public String makeRequest(HashMap<String, 
                          String> requestParams, 
                          HashMap<String, String> requestHeaders, 
                          String method, String URL) 
                          throws IOException {

        FormBody.Builder formBuilder = new FormBody.Builder();

        // Setting request parameters:

        for (Map.Entry<String, String> param : requestParams.entrySet()) {
            formBuilder.add(param.getKey(), param.getValue());
        }

        RequestBody formBody = formBuilder.build();
        Request.Builder requestBuilder = new Request.Builder();

        // Setting request headers:

        for (Map.Entry<String, String> header : requestHeaders.entrySet()) {
            requestBuilder.addHeader(header.getKey(), header.getValue());
        }

        // Setting request method:

        if (method.toUpperCase() == "POST"){
            requestBuilder.post(formBody);
        } else if(method.toUpperCase() == "PUT"){
            requestBuilder.put(formBody);
        } else if(method.toUpperCase() == "DELETE"){
            requestBuilder.delete(formBody);
        } // GET is the default method and doesn’t need to be added.

        Request request = requestBuilder
                .url(URL)
                .build();

        // Getting the response:
        Response response = client.newCall(request).execute();

        if (!response.isSuccessful())
            throw new IOException("Unexpected code " + response);

 
        // Here you could parse, print or return the response as needed, but remember the response can only be consumed directly ONCE:

        // this.parse(response.body().string()); OR
        // return response.body().string(); OR
        // System.out.println(response.body().string());

        // We could also store it in a variable and use it as needed
    }

```

Now, let’s talk about parsing our response, for which I added this handy method to my HttpClient class:

 
```
    protected String parse(String responseBody, String key) {
        JSONObject json = new JSONObject(responseBody);

        String parsedString = json.getString(key);

        return parsedString;
    }

```

This method as it is is useful for a simple response (not nested), and will find the value for a key and return it as a String. In my case, I used it to parse a token that I could use for authentication.

 
Something I didn’t quite understand at the beginning is that the **response can only be consumed once**. This means that you can only have one statement that uses the response (response.body().string()) directly. If for example you add a print statement that also prints that response, we will get a not particularly informative error. 

 To unit test this code, I would recommend the library MockWebServer, you can find a [tutorial here](https://www.testim.io/blog/how-to-use-mockwebserver/), [here](https://github.com/square/okhttp/tree/master/mockwebserver) and [here](https://howtodoinjava.com/java/library/mockwebserver-junit-webclient/).


 <p><img src="/assets/karina-vorozheeva-rW-I87aPY5Y-unsplash.jpg" alt="Cat with a blue batterfly on its nose" width="300"></p>