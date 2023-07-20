# render-phonebook
link to deploy on Render: https://render-phonebook-8ggf.onrender.com/api/persons

To deploy back-end Express app on render
  1. create new web service on Render sie
  2. have Express project in root directory of repo
  3. build instructions: `npm install`
  4. start instructions `npm start`

Change `index.js` file to reflect current PORT from environmental variabl
```javascript
const PORT = process.env.PORT || 3001
app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`)
})
```



To deploy also the front-end React app:
  1. change baseURL in `services/persons.js` = `const baseURL = '/api/persons'`
  2. run `npm run build` in front end app
  3. add build folder to root directory of back-end app
  4. add `static` middleware to Express app `app.use(express.static('build'))` to allow express to show static content