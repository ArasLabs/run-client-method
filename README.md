# Run Client Method

This package adds a method and action to run client-side Methods from the method editor, similar to the built-in Run Server Method action.

## Project Details

See [TESTSTATUS file](./TESTSTATUS.md) for latest testing information.

#### Built Using:
Aras 11.0 SP7

#### Versions Tested:
Aras 11.0 SP7, Aras 11.0 SP5 (open release)

#### Browsers Tested:
Internet Explorer 11, Firefox 38 ESR, Chrome

> Though built and tested using Aras 11.0 SP7, this project should function in older releases of Aras 11.0 and Aras 10.0.

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. RunClientMethod import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\RunClientMethod\Import\imports.mf` file in the Manifest File field.
6. Select **RunClientMethod** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.
10. (Optional) Execute the contents of [Data\testData.xml](./Data/testData.xml) in Nash or AML Studio to add sample data to your database for testing.

You are now ready to login to Aras and try out the Run Client Method action.

## Usage

1. Log in to Aras as admin.
2. Navigate to **Administration > Methods** in the table of contents (TOC).
3. Search for a client method you would like to test and open it.
  * The optional test data contains a method for testing called "test run client method".
4. Click **Actions > Run Client Method** in the main menu.

The Run Client Method action will display a window with the output returned by the method. If the method does not return a value, the window will be blank.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Original code written by Jon Hodge for Aras Professional Services.

Documented and published by Eli Donahue for Aras Labs. @EliJDonahue

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
