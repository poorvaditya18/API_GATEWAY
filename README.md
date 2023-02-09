## API GATEWAY REPOSITORY

- Frontend ---> Middlend ---> Backend
- We need an intermediate layer between the client side and the microservices.
- Using this Middlend , when the client sends request we will be able to make the decision that which microservice will actually respond to this request.
- Apart from this we can do various things such as Message Validation , Response Transformation , Rate limiting 
- We can prepare the Api Gateway that acts as this middle end.
- So basically this is a gateway which routes the request to various services.

- How this is  different from load balancer ?
- Load balancer dont have any logic as such on its own. It's only job is to redirect the request to the application server.
- Ex : Cloud hosting services such as AWS helps you with this.

- Morgan is the npm package . Kind of logger middleware.

- Proxy : what is proxy ? suppose your service is located at localhost:3000 , one way to access this is the user will request to localhost:3000/api/v1 . Problem with this is that at the client side every time client needs to feed this address . We can resolve that using http-proxy-middleware.

- Ex : app.use('/api', createProxyMiddleware({ target: 'http://www.example.org', changeOrigin: true }));
-  http://localhost:3000/api/foo/bar -> http://www.example.org/api/foo/bar
- In the above case now whenever the client will request for /api with localhost as prefixe it will automatically change it to the www.example.com . 