# Serialising-with-replqcer-function-
 
const userRecords = [
 {name: "Joe", points: 14.9, level: 31.5},
 {name: "Jane", points: 35.5, level: 74.4},
 {name: "Jacob", points: 18.5, level: 41.2},
 {name: "Jessie", points: 15.1, level: 28.1},
];
// Remove names and round numbers to integers to anonymize records before sharing
const anonymousReport = JSON.stringify(userRecords, (key, value) =>
 key === 'name'
 ? undefined
 : (typeof value === 'number' ? Math.floor(value) : value)
);
