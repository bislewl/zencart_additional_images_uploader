#Additional Images Uploader
For ZenCart 1.5.5f


##Install
1. BACKUP
2. If in doubt verify 1
3. Copy Files from YOUR_ADMIN into your admin directory
4. Load Admin (module will self install)

*Optional Core Modification*

This Allows access via the product listing page 
1. If desired open your YOUR_ADMIN/includes/modules/category_product_listing.php
2. Find:
 
 `<?php echo '<a href="' . zen_href_link($type_handler, 'cPath=' . $cPath . '&product_type=' . $products->fields['products_type'] . '&pID=' . $products->fields['products_id']  . '&action=new_product' . (isset($_GET['search']) ? '&search=' . $_GET['search'] : '')) . '">' . zen_image(DIR_WS_IMAGES . 'icon_edit.gif', ICON_EDIT) . '</a>'; ?>`
 
 Add After:
 `<?php echo '<a href="' . zen_href_link(FILENAME_ADDITIONAL_IMAGES_UPLOADER, 'product_id=' . $products->fields['products_id'] ) . '"><i class="fa fa-upload"></i></a>'; ?>`

##Usage
1. Go to Tools->Upload Additional Images
2. Search for the product, products_id, products_name, or products_model
3. Click on the correct choice to the right
4. Add Image box should appear click choose file
5. Click Upload
Repeat Steps 4 & 5 for all images, there is no need to re-search each time. 


##Uninstall
1. Remove Files
2. In the admin Tools -> Sql Patches run the uninstall.sql