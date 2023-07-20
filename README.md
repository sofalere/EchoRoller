# render-phonebook
link to backend deploy on Render: https://render-phonebook-8ggf.onrender.com/api/persons

Notes:
To deploy Express app on render
  1. create new web service on Render sie
  2. have Express project in root directory of repo
  3. build instructions: `npm install`
  4. start instructions `npm start`

Change `index.js` file to reflect current PORT from environmental variabl
``javascript
`const PORT = process.env.PORT || 3001
app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`)
})
```
