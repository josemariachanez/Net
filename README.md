# Net
Net.jm

const request = require('request');

const options = {
  method: 'POST',
  url: 'https://api.netflix.com/signup',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    email: 'user@example.com',
    password: 'password123',
    firstName: 'John',
    lastName: 'Doe'
  })
};

request(options, function (error, response, body) {
  if (error) {
    console.error('Error creating Netflix user account: ', error);
  } else {
    console.log('Netflix user account created successfully: ', body);
  }
});
