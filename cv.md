# Junior JavaScript Developer Resume

**Timofei Petrov**  
Nizhny Novgorod, Russia  
[Telegram](https://t.me/spectral_wind) | [Email](mailto:timofey1992@gmail.com)  

#### PERSONAL SUMMARY

Responsible, detail-oriented and hard working person. I am looking for a junior 
position of javascript developer that will allow me constantly improve my skills 
in coding, testing applications, problem solving. I want to learn how to work in a 
team of talented IT professionals. I would like to join a company where thanks to 
teamwork we will create applications to the highest standards.

#### SUMMARY OF SKILLS

* Understanding of web-related technologies such as HTML5, CSS3, DOM, RESTful API
* Basic knowledge: JavaScript, Bootstrap, React, Node.js, npm, Babel, Git
* Knowledge of Linux operating system. OS Windows at the system administrator level
* Understanding of software development life cycle
* Ability to read and understand documentation
* Can work independently and under the direction

#### CODE EXAMPLES

##### (React) Calculation of the position of human face based on Clarifai API:
```javascript
calculateFaceLocation = (data) => {
    const clarifaiFace = data.outputs[0].data.regions[0].region_info.bounding_box;
    const image = document.getElementById('inputimage');
    const width = Number(image.width);
    const height = Number(image.height);
    return {
      leftCol: clarifaiFace.left_col * width,
      topRow:  clarifaiFace.top_row * height,
      rightCol: width - (clarifaiFace.right_col * width),
      bottomRow: height - (clarifaiFace.bottom_row * height)
    }
  }
```
##### (Node.js) Registration for new users using hash passwords:
```javascript
app.post('/register', (req, res) => {
  const {email, name, password} = req.body;
  bcrypt.hash(password, saltRounds, function(err, hash) {
    console.log(hash);
  });
  database.users.push({
    id: '125',
    name: name,
    email: email,
    password: password,
    entries: 0,
    joined: new Date()
  })
  res.json(database.users[database.users.length-1]);
})
```