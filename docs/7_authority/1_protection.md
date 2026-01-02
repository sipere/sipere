---
sidebar_position: 1
---

# Route protection

We can set authentication for each endpoint in the api.js file.

For the get(), post(), put(), patch() or delete() methods, set the verifyToken middleware as the second parameter. This will ensure that the endpoints are only accessible after authentication.

In our example, in square brackets is:

```javascript
[verifyToken]
```

One route protected:

```javascript
router.get('/employees', [verifyToken], EmployeeController.index);
```

All methods are protected:

```javascript
router.get('/employees', [verifyToken], EmployeeController.index);
router.get('/employees/:id', [verifyToken], EmployeeController.show);
router.post('/employees', [verifyToken], EmployeeController.store);
router.put('/employees/:id', [verifyToken], EmployeeController.update);
router.delete('/employees/:id', [verifyToken], EmployeeController.destroy);
```

If we set up protection for a route, we need to log in with the login endpoint before accessing it. We received a token that needs to be sent back to access the protected route.
