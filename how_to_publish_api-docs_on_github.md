#How To Publish Slate API documentation on Github

The editing and publishing system adopted to distribute Yonder API specification is based on [slatedocs/slate](https://github.com/slatedocs/slate).
The current documentation is published at the following address [http://yonderlabs.github.io/api-docs/](http://yonderlabs.github.io/api-docs/).

##First time install
The first time you publish on your documentation on [Github Pages](https://pages.github.com) all you need to do is:

1. login in into yonderlabs [Github](https://github.com) account;
2. search for the [slatedocs/slate](https://github.com/slatedocs/slate) project;
3. fork it;
4. rename the project in the "Settings" menu with the PROJECT_NAME that should appear in the end point of the documentation pages address, (e.g., if PROJECT_NAME="api-docs" the end point will become [http://yonderlabs.github.io/api-docs/](http://yonderlabs.github.io/api-docs/)).
5. clone the repo on your local machine by running the following command from the destination directory:

```
#Clone the documentation repository
git clone git@github.com:yonderlabs/PROJECT_NAME.git
```

Now you just need to replace the source files in the repository, copying and pasting from the documentation source directory into the cloned documentation repository, as described in the next section.


##Update API documentation with Docker
This step must be repeated every time we want to update the public API documentation. The following directions 
refer to the use of slate in Docker. The advantage provided by this method is that you need to install only Docker and git, you do not need to install on your local machine, Ruby and all other dependencies.
Dettailed information can be found at [slatedocs/slate/Docker](https://github.com/slatedocs/slate/wiki/Using-Slate-in-Docker).

###Update
1. If you don't have it already, clone the repo on your local machine by running the following command from the destination directory:

```
#Clone the documentation repository
git clone git@github.com:yonderlabs/PROJECT_NAME.git
```
2. update, replace or add  files in the cloned source directory;

###Build
The updated web pages can be generated through Docker,  To do that run the following commands.

```
#Change to the project Directory
cd PROJECT_NAME

#Let Docker build the .html pages
docker run --rm --name slate -v $(pwd)/build:/srv/slate/build -v $(pwd)/source:/srv/slate/source slatedocs/slate
```
 
###Test
When the new pages are ready it is possible to check them locally. To do that run the following commands:

```
#Change to the project Directory
cd PROJECT_NAME

#Use Docker to render the pages on a local server
docker run --rm --name slate -p 4567:4567 -v $(pwd)/source:/srv/slate/source slatedocs/slate serve
```
Now you will be able to access your site at  [http://localhost:4567](http://localhost:4567)
 
###Publish on github
To publish the new documentation on [http://yonderlabs.github.io/PROJECT_NAME/](http://yonderlabs.github.io/PROJECT_NAME/) run the following command:

```
#Change to the project Directory
cd PROJECT_NAME

#Only deploy the pages generated in the build directory
./deploy.sh --push-only
```
###Commit the updated documentation
When you are done with the documentation update you need to store the new content in the git repository by running the following commands:

```
#Enter the project root
cd PROJECT_NAME
#Add all files 
git add .
git commit -a -m "this is an example of commit comment message."
git push
```
Note: this will only update the github repo, we have to understand how to sync our private repo on gitlab.

##Note
1. Sometimes the update of github takes quite some time (seconds?), be patient!
2. Beside the specific documentation files, with respect to the default slate settings the following files have been modified:

```
- PROJECT_NAME/source/stylesheets/_variables.scss
- other?
```