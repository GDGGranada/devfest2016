# GDG Devfest Granada 2016


![preview-web](https://cloud.githubusercontent.com/assets/2954281/17777476/5dbbbe1c-6569-11e6-9cc4-77185ae9bf92.png)

# Current progress

GDG Granada team were started working to custom this app.



# Project Hoverboard 

> Project Hoverboard is the next generation conference website template after 
[Project Zeppelin](https://github.com/gdg-x/zeppelin) and more optimized 
version - [Project Zeppelin-Grunt](https://github.com/gdg-x/zeppelin-grunt).

> Template is brought by [Oleh Zasadnyy](https://plus.google.com/+OlehZasadnyy) 
from [GDG Lviv](http://lviv.gdg.org.ua/).

> *Do you :heart: it?* Show your support - please, :star: the project.


### Setup
:book: [Full documentation](/docs/).

##### Docker based development env

If you don't want to bother with the dependencies, you can develop in the docker container.

Build:

    docker build -t hoverboard .

and run:

    docker run -it -v "$PWD":/app -p 8080:8080 hoverboard

:book: Read more in [docker docs](/docs/tutorials/docker.md).

###### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm i -g polymer-cli
    
and [Bower](https://bower.io/):
    
    npm i -g bower
    
:point_right: **[Fork](https://github.com/gdg-x/hoverboard/fork) this repository** and clone it locally.

##### Install dependencies

    bower install

##### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve
    
:book: Read more in [setup docs](/docs/tutorials/set-up.md).


### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build

Or you can build in Docker container:

    docker run -v "$PWD":/app hoverboard polymer build
    
:book: Read more in [deploy docs](/docs/tutorials/deploy.md).   

### Updating
Here is a git workflow for updating your fork (or downloaded copy) to the latest version:
```
git remote add upstream https://github.com/gdg-x/hoverboard.git
git fetch upstream
git merge upstream/master # OR git merge upstream/develop
# resolve the merge conflicts in your editor
git add . -u
git commit -m 'Updated to the latest version'
```

### Contributing

Project Hoverboard is still under development, and it is open for contributions. 
Feel free to send PR. If you have any questions, feel free to contact 
[Oleh Zasadnyy](https://plus.google.com/+OlehZasadnyy).

##### General workflow
1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Make your changes
4. Run the tests, adding new ones for your code if necessary
5. Commit your changes (`git commit -am 'Added some feature'`)
6. Push to the branch (`git push origin my-new-feature`)
7. Create new Pull Request

:book: Read complete [contributing guide](CONTRIBUTING.md).


### Contributors :sparkles:
See [list of contributors](https://github.com/gdg-x/hoverboard/graphs/contributors).

__Maintainer:__ [Oleh Zasadnyy](https://github.com/ozasadnyy) and [Sophie Huts](https://github.com/sophieH29).


######The GDG App, GDG[x] are not endorsed and/or supported by Google, the corporation.


### License

Project is published under the [MIT license](https://github.com/gdg-x/hoverboard/blob/master/LICENSE.md).  
Feel free to clone and modify repo as you want, but don't forget to add reference to authors :)
