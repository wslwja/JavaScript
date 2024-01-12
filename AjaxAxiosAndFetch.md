
Differences among ajax, axios, and fetch

（1）AJAX

jax is called "AsynchronousJavascriptAndXML" (asynchronous JavaScript and XML), 
which refers to the creation of interactive web pagethe web page development technology of the application. 
It is a technology that can update some web pages without reloading the entire web page.
By exchanging a small amount of data with the server in the background, Ajax can make web pages update asynchronously. 
This means that some parts of the webpage can be updated without reloading the entire webpage. Traditional web pages (without Ajax) must be overloaded if content needs to be updated. 
Its disadvantages are as follows: 
●it is designed for MVC programming and does not conform to the tide of front-end MVVM. 
●based on native XHR development, the XHR architecture is unclear. 
●does not conform to the principle of Separation of Concerns (Separation of Concerns) 
●the configuration and calling methods are very confusing, and the event-based asynchronous model is not friendly. 

（2）Fetch
fetch, known as a substitute for AJAX, appeared in ES6 and used promise objects in ES6. 
Fetch is designed based on promise. The code structure of Fetch is much simpler than that of ajax. 
fetch is not a further encapsulation of ajax, but a native js without using XMLHttpRequest objects. 

fetch的优点：
The advantages of fetch:
●simple syntax and more semantic 
●based on standard Promise, async/await is supported. 
●more underlying, provides a variety of APIs (request, response) 
●separated from XHR, it is a new implementation method in ES Specification. 

fetch的缺点：
Disadvantages of fetch: 
●fetch only reports errors for network requests and regards 400,500 as successful requests. When the server returns 400,500 error codes, it will not reject the requests. fetch will only be rejected if the requests cannot be completed due to network errors.
●fetch(url, {credentials: 'include'}) by default, fetch does not contain cookies. You need to add a configuration item: fetch(url, {credentials: 'include'}) 
●fetch does not support abort or timeout control. The timeout control implemented by setTimeout and Promise.reject cannot prevent the request process from continuing to run in the background, resulting in waste of traffic. 
●fetch cannot locally monitor the progress of the request, while XHR can


（3）Axios
Axios is an HTTP client encapsulated based on Promise. Its features are as follows:
●the browser initiates a XMLHttpRequests request. 
●the node initiates an http request. 
●support Promise API 
●listening requests and responses
●convert requests and responses 
●cancel the request 
●automatically convert json data
●the client can defend against XSRF attacks.
