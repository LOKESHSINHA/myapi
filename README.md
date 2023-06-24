// Importing the 'http' module
const http = require('http');

// Importing the 'data' module from a local file
const data = require('./data');

// Creating an HTTP server
http.createServer((req, resp) => {
  
  // Setting the response header with status code 200 and content type as JSON
  resp.writeHead(200, { 'Content-type': 'application/json' });
 
  // Writing the JSON representation of the 'data' object to the response
  resp.write(JSON.stringify(data));
  
  // Ending the response
  resp.end();
}).listen(7000); // Listening on port 7000



const data = [
  // Array of bank branch objects
  { bank: 'State Bank of India', branch: 'Mumbai Main', name: 'Rahul Sharma', ifsc: 'SBIN0001234' },
  { bank: 'ICICI Bank', branch: 'Chennai Branch', name: 'Sneha Patel', ifsc: 'ICIC0005678' },
  { bank: 'HDFC Bank', branch: 'Delhi Connaught Place', name: 'Amita Desai', ifsc: 'HDFC0009123' },
  { bank: 'Axis Bank', branch: 'Kolkata Park Street', name: 'Vikram Banerjee', ifsc: 'UTIB0004567' },
  { bank: 'Punjab National Bank', branch: 'Bengaluru MG Road', name: 'Kavita Rao', ifsc: 'PNBK0007890' },
  { bank: 'Bank of Baroda', branch: 'Hyderabad Banjara Hills', name: 'Rajeshwari Reddy', ifsc: 'BARB0002345' },
  { bank: 'Canara Bank', branch: 'Ahmedabad C.G. Road', name: 'Aruna Patel', ifsc: 'CNRB0006789' },
  { bank: 'Union Bank of India', branch: 'Pune FC Road', name: 'Nikhil Joshi', ifsc: 'UBIN0003412' },
  { bank: 'Indian Bank', branch: 'Jaipur MI Road', name: 'Priya Gupta', ifsc: 'IDIB0005678' },
  { bank: 'IDBI Bank', branch: 'Lucknow Gomti Nagar', name: 'Rajesh Verma', ifsc: 'IBKL0009012' }
];

// Exporting the 'data' array as a module
module.exports = data;
