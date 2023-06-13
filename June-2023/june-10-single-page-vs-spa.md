# Single Page Apps Vs SPA's, and Testing With Various Tools
The structure of the Angular project is different from the Express HTML page primarily by how HTML pages are sent from the server and rendered on the browser. In the Express version, when a user visits a different page, a new page is requested from the server and a unique HTML page is sent back with all or most of the information they need. With an Angular SPA, single-page application, only one HTML page is sent as a template, and JavaScript in the form of Angular changes the HTML. When a user goes to a new page or URL, the HTML page is manipulated on their browser and any remaining data needs are requested through the server.

The advantage of SPA’s is that they have a more reactive experience and less load on the servers. User’s can quickly switch pages and load new parts of an app without relying on internet speed more than their own machine’s processing power. This also means the client browser does the heavy lifting of rendering all the HTML pages according to the user’s needs. The disadvantages compared to a simpler web app interaction is the performance of the user’s machine and the load time. Since most of the needed data is stored code, the browser must load all this code and run it, which can take several seconds depending on the size of the application. Also, if many components are rendered needlessly on the browser, the experience for the user can be slower than expected. 

What helped me test the SPA was using Postman, MongoDB’s Compass, and the console. Postman allowed me to look into the API requests and understand what happened and what data was passed for what reason, and whether it was successful. Compass allowed me to see the data and make sure that it added unique data properly and completely. The console in the frontend and backend allowed me to handle the errors I ran into, such as when I implemented the Delete operation, it had an error on the response data conversions. This error was caused by the re-render of the edit-trip component, and so I fixed it by checking for the data response.