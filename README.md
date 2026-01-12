// Contoh cara pakai (JavaScript)
const operators = require('./id-phone-prefix.json');

function detectOperator(phoneNumber) {
    // Ambil 4 digit pertama (misal: 0812)
    const prefix = phoneNumber.substring(0, 4);
    const result = operators.find(item => item.prefix === prefix);
    return result ? result.operator : "Unknown Operator";
}

console.log(detectOperator("08123456789")); // Output: Telkomsel
