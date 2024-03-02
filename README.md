# Net
Net.jm
function generateNetflixCode(length) {
  // Define the possible characters for the code
  const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';

  // Create an empty string to hold the code
  let code = '';

  // Generate the code by selecting random characters from the possible characters
  for (let i = 0; i < length; i++) {
    code += characters.charAt(Math.floor(Math.random() * characters.length));
  }

  // Return the generated code
  return code;
}

// Generate a 6-character Netflix code
const netflixCode = generateNetflixCode(6);
console.log(netflixCode);
