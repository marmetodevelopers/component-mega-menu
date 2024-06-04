# Mega Menu Component

The mega menu component has built as it is one of the most curical navigation elements on an e-commerce store. These kind of menus display additional information, links to top selling products and collections, promotional banners and more to boost the sales of the e-commerce store!

The mega menu component built here is very website performance friendly as the mega menu section is lazyily loaded, hence reducing DOM size and improving the performance of the website!

**Live Preview Link**: https://fozail-ahmad-store.myshopify.com/?preview_theme_id=136197931189

**Customizer Link:** https://admin.shopify.com/store/fozail-ahmad-store/themes/136197931189/editor

## Features

 - Feature 1 Option to link a mega menu to a header navigation element based on its title (case-sensitive)
 - Feature 2 Options for adding mega menu heading and subheading
 - Feature 3 Option to link menu from the backend navigation
 - Feature 4 Option to add an image with image heading and subheading
 - Feature 5 Option for mega menu button text and link
 - Feature 6 Block option for menu item icon
 - Feature 7 Block options for link heading, link description and link URL 
   
## Dependencies

 - Dependency 1 Implementation of lazy loaded sections

## Implementation Steps

Read and understand the implementation steps for the mega menu element for the smooth functioning as it has been implemented in 3 curical steps:-

 - ### Step 1: Backend implementation
	- 1.1 In your header component, link a main menu accordingly to the project requirement.
	- 1.2 This section is lazy loaded and will link to the header menu if the header menu has child links (1st level links). For example in the preview link, the main menu has 'shop' mega menu. So for this 'shop' navigation link to have a mega menu linked, we need to add a child link as a placeholder so that the mega menu section has a base to get linked. Please refer the main menu screenshot below.
        - ![Screenshot (237)](https://github.com/marmetodevelopers/component-mega-menu/assets/155415315/8d7fd401-004b-4076-9742-ed5dfef45514)
        - Once this is done, the backend implementation for the mega menu is completed!

  - ### Step 2: Lazy loaded section implementation
	- 2.1 global.js - copy/paste the code for the lazy section custom element from line 1836 to line 1943 into your global.js file in your theme!
 	- 2.2 lazy-load-section-validations.liquid snippet -  Create/Add a new snippet file under the snippets folder and copy/paste the code from 'lazy-load-section-validations.liquid'
  	- 2.3 settings_schema.json - Add line 10 to 56 into your settings_schema.json file in your theme!

  - ### Step 3: Frontend implementation
	- 3.1 header.liquid section - Add line 180 to 188 into your header.liquid file in your theme! (This is done to initalize the mega menu usage)
 	- 3.2 header-mega-menu.liquid snippet - Create/Add a new snippet file under the snippets folder and copy/paste the code from 'header-mega-menu.liquid'
  	- 3.3 megamenu-item-demo-1.liquid section - Create/Add a new section under the section folder and copy/paste the code from 'megamenu-item-demo-1.liquid'
	- 3.4 component-mega-menu.css - Create/Add a new css file under the asset folder and copy/paste the code from 'component-mega-menu.css'
	- 3.5 details-disclosure.js - add the HeaderMenu custom element into your existing details-disclosure.js file in your theme!
	- 3.6 'javascript-injected-section.js' - Create/Add a new js file under the asset folder and copy/paste the code from 'javascript-injected-section.js'
   	- 3.7 The final step would be to add the link heading (The mega menu will appear below this parent link), it should be the same as the element which has the placeholder child link in the navigation menu mentioned in step 1.2 (case-sensitive)

# Important Notes

>  - The component employs its own styling for the grid system. For further optimization, consider using the classes provided by the
> theme.
