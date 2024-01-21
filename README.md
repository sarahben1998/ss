1)Average of Even Numbers using filter() and reduce():

function averageOfEvenNumbers(numbers) {
  const evenNumbers = numbers.filter(num => num % 2 === 0);
  const sum = evenNumbers.reduce((acc, num) => acc + num, 0);
  
  return evenNumbers.length === 0 ? 0 : sum / evenNumbers.length;
}

// Example usage:
const numbersArray = [1, 2, 3, 4, 5, 6];
const average = averageOfEvenNumbers(numbersArray);
console.log(average); // Output: 3.5
Longest Word using reduce():

2)function longestWord(words) {
  return words.reduce((longest, current) => (current.length > longest.length ? current : longest), '');
}

// Example usage:
const wordsArray = ["apple", "banana", "kiwi", "strawberry"];
const longest = longestWord(wordsArray);
console.log(longest); // Output: "strawberry"



3)Average Number of Pages using map() and reduce():

function averagePages(books) {
  const totalPages = books.map(book => book.pages).reduce((acc, pages) => acc + pages, 0);
  return books.length === 0 ? 0 : totalPages / books.length;
}

// Example usage:
const booksArray = [
  { title: "Book1", author: "Author1", pages: 100 },
  { title: "Book2", author: "Author2", pages: 150 },
  { title: "Book3", author: "Author3", pages: 120 }
];
const averagePagesResult = averagePages(booksArray);
console.log(averagePagesResult); // Output: 123.33333333333333

4)Frequency of Strings using reduce():

function stringFrequency(strings) {
  return strings.reduce((freqObj, str) => {
    freqObj[str] = (freqObj[str] || 0) + 1;
    return freqObj;
  }, {});
}

// Example usage:
const stringsArray = ["hello", "world", "hello"];
const frequencyObj = stringFrequency(stringsArray);
console.log(frequencyObj); // Output: { hello: 2, world: 1 }


5)Count of People by City using reduce():

function countPeopleByCity(people) {
  return people.reduce((cityCount, person) => {
    const city = person.city;
    cityCount[city] = (cityCount[city] || 0) + 1;
    return cityCount;
  }, {});
}

// Example usage:
const peopleArray = [
  { name: "Alice", age: 30, city: "New York" },
  { name: "Bob", age: 40, city: "Chicago" },
  { name: "Charlie", age: 50, city: "New York" }
];
const cityCountObj = countPeopleByCity(peopleArray);
console.log(cityCountObj); // Output: { "New York": 2, "Chicago": 1 }
