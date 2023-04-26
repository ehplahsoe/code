// A function that generates a random password
function generatePassword(length) {
  const charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
  let password = "";
  for (let i = 0; i < length; i++) {
    password += charset.charAt(Math.floor(Math.random() * charset.length));
  }
  return password;
}

// Example usage
console.log(generatePassword(12)); // Output: "2iNzjK63rX9L"

// A class representing a shopping cart
class ShoppingCart {
  constructor() {
    this.items = [];
  }
  addItem(item) {
    this.items.push(item);
  }
  removeItem(item) {
    const index = this.items.indexOf(item);
    if (index !== -1) {
      this.items.splice(index, 1);
    }
  }
  getTotal() {
    return this.items.reduce((total, item) => total + item.price, 0);
  }
}

// Example usage
const cart = new ShoppingCart();
cart.addItem({ name: "Shirt", price: 20 });
cart.addItem({ name: "Pants", price: 30 });
console.log(cart.getTotal()); // Output: 50
