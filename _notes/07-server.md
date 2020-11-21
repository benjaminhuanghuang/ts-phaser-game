
## Server


```
// isolated in the public folder
app.use(express.static('public'));

// When the user visits our domain with no sub-domain. We shall serve them
// our index.html file that contains the game and our login screen.
app.get('/', (req, res) => {
  res.sendfile(`./index.html`);
});
```


## Socket.IO
