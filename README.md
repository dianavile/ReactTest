# ReactTest
Code snippets to practice React

# Composition
// Create a getProfileLink() function
```
function getProfileLink (username) {
  return 'https://github.com/' + username
}
```
// Create a getProfilePic() function
```
function getProfilePic (username) {
  return 'https://github.com/' + username + '.png?size=200'
}
```
// COMPOSE BOTH FUNCTIONS (=combine them together inside another function)
```
function getProfileData (username) {
  return {
    pic: getProfilePic(username),
    link: getProfileLink(username)
  }
}
```
OR // WRITE getProfileData WITHOUT COMPOSITION (providing the data directly)
```
function getProfileData (username) {
  return {
    pic: 'https://github.com/' + username + '.png?size=200',
    link: 'https://github.com/' + username
  }
```
__NOTE:__ Potential issues with version WITHOUT composition:
- 1) 
- 2) 
