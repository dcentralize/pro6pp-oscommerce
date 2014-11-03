pro6pp-oscommerce
==============

The repository of the \*.diff files as well as the new files that are extracted after integrating
the Pro6PP service into osCommerce.

## How to install

### Get the diff files from Github with either of the two available ways.

* `git clone`
* Download the repository as a .zip file
* Extract or open the pro6pp-oscommerce folder
* Copy or open the folder with the name equal to the osCommerce version you have installed.

### Apply the patches to your osCommerce installation

The folder of your version contains a .patch file and seperate .diff files.

If you are using a default installation of osCommerce, you can simply apply the .patch file (from the root folder of your installation).

```bash
#i.e. pwd:/var/www/html/my_oscommerce_site/
patch -p1 < /path/to/pro6pp_osComm_v*.*.*.patch
```

Otherwise, if you have customized any files, you will have to manually apply
the patches yourself using the provided `.diff` files.

```shell
patch path/to/original/file path/to/pro6pp/diff/file
```

If the above command fails during execution, you can revert the patch

```shell
patch -R path/to/original/file path/to/pro6pp/diff/file
```

And open the diff files in order to do the changes via the text editor of your 

__Note__: Copy the autocomplete.js file into the root of your website if you don't have it already.
