# wordpress-simple-lightbox

A super-simple minimalist lightbox utilising core Wordpress gallery shortcodes.

This lightbox was initially created for the Eat Sleep Knit site, which utilises the Wordpress core gallery shortcodes for inserting more than one image into a page.

Rather than dealing with a bulky-looking lightbox or modal pop-up, I simply created a nice transition effect which loads the image at a larger size onto the page and fades in and out. 

It really is no frills. See it in action by clicking on pictures in the main article here: http://www.eatsleepknit.co.uk/butterick-6185-collared-blouse-review/

## How the HTML looks

The gallery shortcodes can be handwritten using IDs, or inserted into a page using the Wordpress media uploader. Just select however many gallery images you want on the page in one set and insert. This inserts a div with the class `gallery` which all image elements are nested into.

	<div id="gallery-1" class="gallery galleryid-728 gallery-columns-1 gallery-size-medium">
	  <dl class="gallery-item">
		  <dt class="gallery-icon landscape">
				<img src="http://www.eatsleepknit.co.uk/wp-content/uploads/2015/05/11202903.jpg">
			</dt>
		</dl>
	</div>
	
My code firstly gives the image a class of `gallery-icon` on the image wrapper. This means I can add a little magnifying class icon to let the user know they can zoom.

Importantly, embedded into all post pages is a modal pop-up div ready for content to be loaded in, which is hidden by default:

	<div class="modal-wrap" style="display:none;">
	  <div class="gallery-modal"></div>
	</div>

## Javascript listener


