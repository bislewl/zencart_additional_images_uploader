============ Additional Images Uploader for Zen Cart - Version: 1.0.2 ============

This module is an Beginner installation for Zen Cart 1.5.6b, although it may 
work on other 1.5.X versions. This module was tested on PHP 5.7.26 and 
MySQL 5.7.26. 

=============== Description ===============

This module allows you to search for a product by name, model and ID for a product
that you wish to add additional images to. Then you select the product from the 
right hand side results list to add images to.

Now the browse button appears. Browse, select your image and click the upload 
button. The interface is ajax powered so you can upload many images, very quickly.

The module correctly names the images in the required Zen Cart naming fashion,
so that your images display in your template properly.

All of this is done with ZERO template changes, ZERO overwritten files and ZERO 
headache of the current available modules.

There is instructions below to add an icon in the admin product index lists to
shortcut the functionality, optionally, as well.

=============== Installation Instructions ===============

1. BACKUP your files and database.
2. If in doubt verify step 1.
3. Copy Files from YOUR_ADMIN into your own admin directory, 
   there are no overwrites.
4. Load or reload your Zen Cart admin and module will self install.
  
PRE 1.5.6 Versions:
1. Upload the ajax.php file into your admin directory. This isn't needed as 1.5.6 now supports this
2. Move the File 
============= OPTIONAL Core Modification =============

This modification allows access via the admin product listing page.
 
Open your YOUR_ADMIN/includes/modules/category_product_listing.php 

FIND
<?php echo '<a href="' . zen_href_link($type_handler, 'cPath=' . $cPath . '&product_type=' . $products->fields['products_type'] . '&pID=' . $products->fields['products_id']  . '&action=new_product' . (isset($_GET['search']) ? '&search=' . $_GET['search'] : '')) . '">' . zen_image(DIR_WS_IMAGES . 'icon_edit.gif', ICON_EDIT) . '</a>'; ?>
 
ADD AFTER
 
<?php echo '<a href="' . zen_href_link(FILENAME_ADDITIONAL_IMAGES_UPLOADER, 'product_id=' . $products->fields['products_id'] ) . '"><i class="fa fa-upload"></i></a>'; ?> 

=============== Uasage ===============

1. Go to Tools->Upload Additional Images
2. Search for the products_id, products_name (or portion of it) or products_model.
3. Click on the correct choice to the right in the search results.
4. Add Image area should appear below click browse to choose file.
5. Click Upload.
Repeat Steps 4 & 5 for all images, there is no need to re-search each time. 

=============== Support ===============

Please direct support questions here (https://pro-webs-support.com/)

The module's master page is here
https://zencart.codes/index.php?main_page=product_info&cPath=32&products_id=92

We can also install this module for you 
https://zencart.codes/index.php?main_page=product_info&cPath=32&products_id=92

=============== Uninstallation Instructions ===============

- Backup your Files and Database.
- Remove the files installed by the module.
- Run the included uninstall.sql in Admin >> Tools -> Sql Patches

===============Version History===============

02/20/2018 1.0.0 PRO-Webs.net - Initial Release
05/09/2018 1.0.1 PRO-Webs.net - Language Changes, ZC Plugin ID Updated
06/15/2019 1.0.2 PRO-Webs.net - File/Directory Changes to support version 1.5.6, with instructions/filed for previous versions

===============Legal===============

By downloading this software you agree to the license included in this package.
PRO-Webs, Inc. declares no responsibility for the use of this module and 
provides no warranty, promise, nor other expectations. Install modules in your
Zen Cart software at your own risk.
