# WAD 2020 Exam 2: Project B

## Project setup
```
npm install
```

### Run your tests
```
npm run test
```
# Setup

You will need to [import](https://docs.github.com/en/free-pro-team@latest/github/importing-your-projects-to-github/importing-a-repository-with-github-importer) 
this repository to you GitHub account, to do that please follow these steps:
* Go to Github [import page](https://github.com/new/import)
  * **Note**: you have to be logged in to your GitHub account
* In the first field `"Your old repository’s clone URL"` enter URL of this repository `https://github.com/tsotnekekelia/wad20-exam2-b`
* In  the next field give it a name
* Make it **Private**
* And begin to import, it should take few seconds
* Add me as a collaborator to your new repository, [click here](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository)
 to learn how
  * My `email` and `username` on github is: `cotne.kekelia@yahoo.com` and `tsotnekekelia`
  
# Tasks
  
Modify [Entries.spec.js](./tests/unit/Entries.spec.js) 
to test the functionality of [Entries.vue](./src/components/Entries.vue) component.
 
**Note:** you need to create and pass some test data to this component in the test file.

1. Test that as many entries are displayed as items in the array that are passed to `Entries` component _**[6 points]**_
  1. One entry is encapsulated in a `li` with class `.entry`
2. Test that dates displayed are in the correct format _**[6 points]**_
  1. **Note:** to make it easy use `moment.js` which is already installed.
3. Test that entries that have `image` property also render image tag, 
and entry objects that do not have `image` property skip rendering of the image tag  _**[10 points]**_
4. Test that reordering button is displayed _**[3 points]**_
  
