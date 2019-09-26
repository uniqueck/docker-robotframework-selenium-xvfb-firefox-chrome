# robotframework-selenium-xvfb-firefox-chrome

Docker image with RobotFramework, SeleniumLibrary, Firefox and Chrome. (With
XvfbRobot library for headless browser testing)

## Usage

If you're standing in the directory with your `.robot` test files, you can
invoke the container using the following command:

```shell
$ docker run --rm -v $(pwd):/robot madworx/robotframework-selenium-xvfb-firefox-chrome 
```

By default, this image places all output into a separate subdirectory, `output/`
relative to the directory you mapped above.

Any arguments you add to the container will be passed on to the `robot` command, so if you e.g. wish to change the output directory to something else, and only run test cases in a specific sub-directory, you could use the following:

```shell
$ docker run --rm -v $(pwd):/robot madworx/robotframework-selenium-xvfb-firefox-chrome --outputdir my-outputdir/ robottests/webtest.robot
```

## Contributing

Any and all contributions are welcome, in the form of 
[pull requests](https://github.com/madworx/docker-robotframework-selenium-xvfb-firefox-chrome/pulls).

## Authors

* **Martin Kjellstrand** - *Initial work* - [madworx](https://github.com/madworx)

## License

This project is licensed under the MIT License - see the
[LICENSE.txt](LICENSE.txt) file for details.
