#How To Publish Slate API documentation on Github

The editing and publishing system adopted to distribute Yonder API specification is based on [tripit/slate](https://github.com/tripit/slate).
The current documentation is published at the following address [http://yonderlabs.github.io/api-docs/](http://yonderlabs.github.io/api-docs/).

##First time install
The first time you publish on your documentation on [Github Pages](https://pages.github.com) all you need to do is:

1. login in into yonderlabs [Github](https://github.com) account;
2. search for the [tripit/slate](https://github.com/tripit/slate) project;
3. fork it;
4. rename the project in the "Settings" menu with the PROJECT_NAME that should appear in the end point of the documentation pages address, (e.g., if PROJECT_NAME="api-docs" the end point will become [http://yonderlabs.github.io/api-docs/](http://yonderlabs.github.io/api-docs/)).
5. clone the repo on your local machine by running the following command from the destination directory:
6. ```
#Clone the documentation repository
git clone git@github.com:yonderlabs/PROJECT_NAME.git
```

Now you just need to replace the source files in the repository, copying and pasting from the documentation source directory into the cloned documentation repository, as described in the next section.


##Update and publish content
This step must be repeated every time we want to update the public API documentation.

1. If you don't have it already, clone the repo on your local machine by running the following command from the destination directory:
2. ```
#Clone the documentation repository
git clone git@github.com:yonderlabs/PROJECT_NAME.git
```
3. replace the files in the cloned source directory with the updated ones from the local source directory;
4. run the following commands:

```
#Enter the project root
cd PROJECT_NAME
#Update the content on remote repo 
git add .
git commit -a -m "this is an example of commit comment message."
git push
#Publish the content on Github pages
rake publish
```


That's it! Now you can enjoy your documents at [http://yonderlabs.github.io/PROJECT_NAME/](http://yonderlabs.github.io/PROJECT_NAME/).

##Note
Sometimes the update of github takes quite some time (seconds?), be patient!