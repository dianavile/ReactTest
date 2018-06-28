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
- 1) __duplicate code__ is needed, but A good function should follow the "DOT" rule: __Do One Thing__
- 2) This function is doing a couple of different (minor) things; 
a) it's creating two different URLs, 
b) storing them as properties on an object, 
c) returning that object. 

WHEREAS: in the composed version, each function just does one thing:

- `getProfileLink` – just builds up a string of the user's GitHub profile link
- `getProfilePic` – just builds up a string the user's GitHub profile picture
- `getProfileData` – returns a new object

__SUMMARY:__
- Write a function WITH COMPOSITION
- Use the DOT RULE: DO ONE THING at the TIME.
- React builds up pieces of a UI using __components__. 
```
<Page />
<Article />
<Sidebar />
```

