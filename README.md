# virtualswift - Swift virtual environment builder.

Virtualswift is a tool for creating isolated 'virtual' swift environments.

If you are familiar with python, then virtualswift is to swift what virtualenv is to python.

## Prerequisites

#### On Ubuntu
You need all dependencies required for the swift language and wget.
The following command should install everything:
`sudo apt-get install clang libicu-dev wget`

#### On Mac
You need to install xcode required by the version of swift you intend to use.
See xcode and macOS versions required for each release of swift [here.](https://swift.org/download/#using-downloads)

As of now, if you have xcode 9 beta or later, you can install only swift 4. I have not figured out a workaround for running multiple versions of swift in different virtual environments on a mac machine. However, on ubuntu you can run different versions of swift in different virtual environments.

## 📚 Installation Steps

###### Automatic Install ######

1. Run `bash <(curl -Ls https://github.com/ankit1ank/virtualswift/raw/master/install.sh)`

2. Verify installation by running `which virtualswift`. If the output looks like the following the installation is successful.

	```
	/usr/local/bin/virtualswift
	```

###### Manual Install ######

1. Clone the repo

	```
	git clone https://github.com/ankit1ank/virtualswift
	```

2. Copy the script to any folder that's in your path variable.

	```
	cd virtualswift
	sudo cp ./virtualswift /usr/local/bin
	chmod +x /usr/local/bin/virtualswift
	rm -rf virtualswift # Delete the cloned repo
	```
3.  Verify installation by running `which virtualswift`. If the output looks like the following the installation is successful.

	```
	/usr/local/bin/virtualswift
	```

## 📚 Usage
1. Create a new virtual environment

	```
	virtualswift myenv
	```

2. Activate the virtualenv.

	```
	cd myenv
	source ./activate
	```

	The command line prompt changes to indicate that the virtual 	environment is activated.

3. You can deactivate the activated virtual environment.

	```deactivate```

By default the latest release of Swift (4.0.2 as of now) will be installed. You can choose a different version of swift as shown below:

```virtualswift myenv 3.1.1```

Supported version numbers: 4.0.2, 4.0, 3.1.1, 3.1

## 👥 Contact Me
Report a bug, Suggest improvements or just say "Hello".

  [@ankitank](https://twitter.com/ankitank)