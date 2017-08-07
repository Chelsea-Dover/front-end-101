# AJAA

AJAX stands for Asynchronous JavaScript And XML.
A technique for loading data into part of a page
without having to refresh the entire page.
This is the secret behind the single-page web
application.

In a nutshell, it is the use of the XMLHttpRequest object to communicate with servers. It can send and receive information in various formats, including JSON, XML, HTML, and text files. AJAX’s most appealing characteristic is its "asynchronous" nature, which means it can communicate with the server, exchange data, and update the page without having to refresh the page.

## making a HTTP request
You use an `XMLHttpRequest` to make the call for you. You first need to a instantiate an object with the necessary functionality. This is what we use `XMLHttpRequest` for.

e.g.
```
var xhr = new XMLHttpRequest();
```

After making a request, you will receive a response back. At this stage, you need to tell the XMLHttp request object which function will handle the response, by setting the onreadystatechange property of the object and naming it after the function to call when the request changes state, like this:

```
httpRequest.onreadystatechange = nameOfTheFunction;
```

Notice how there are no parentheses after the function name. That's because we're assigning a reference to the function, not calling it.

After stating what happens to the response you receive you need to actually make the request but using the methods `open()` and `send()`.

e.g.
```
httpRequest.open('GET', 'data/example.json', true);
httpRequest.send();
```

**open()**
open() has 3 parameters:
1. HTTP Method
2. url of the page handling your request
3. bool for if it should be asynchronous

**send()**
send() is what actually sends the request, and can accept any extra
info you want to send with your call.
This is where you send any additional data you might need to
send with your request

## Handling server response
Remember how we provided the name of a JavaScript function to handle to response when we sent the request?

e.g.
```
httpRequest.onreadystatechange = nameOfTheFunction;
```

What actually goes into that? The first thing the function needs to do is check the request's state. If the request's state is done, that means the full server response has been received and it's okay for you to continue processing it.

e.g.
```
if (httpRequest.readyState === XMLHttpRequest.DONE) {
    // Everything is good, the response was received.
} else {
    // Not ready yet.
}
```

Full list of readyState values are as follows:
 - 0 (uninitialized) or (request not initialized)
 - 1 (loading) or (server connection established)
 - 2 (loaded) or (request received)
 - 3 (interactive) or (processing request)
 - 4 (complete) or (request finished and response is ready)

 Nest we need to check the response code of the HTTP response. Some possible codes are `404` which means  Not Found, or ` 200` which means the request has been successful, the full list of possible codes can be found [here](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html).

 e.g.
 ```
 if (httpRequest.status === 200) {
     // Perfect!
 } else {
     // There was a problem with the request.
     // For example, the response may have a 404 (Not Found)
     // or 500 (Internal Server Error) response code.
 }
 ```

 After we've done that we can do whatever we'd like with the data. The two options to access the data are:

 - httpRequest.responseText: returns the server response as a string of text
 - httpRequest.responseXML: returns the response as an XMLDocument object you can traverse with JavaScript DOM functions

 **Note** the steps above are valid only if you used an asynchronous request (the third parameter of open() was unspecified or set to true). If you used a synchronous request you don't need to specify a function, but this is highly discouraged as it makes for an awful user experience.
