pcommerce.payment.docdata
=======================

pcommerce.payment.docdata is a plone plugin, which provides payment over docdata for PCommerce

You can find it on github at: https://github.com/huubbouma/pcommerce.payment.docdata

By: Huub Bouma (http://www.wyldebeast-wunderliebe.com)

The Docdata specific hashing, status, and exception code was taken from the
**django-docdata** project (https://github.com/dokterbob/django-docdata)
The author of that part of the code is Mathijs de Bruin
he has stated in en email conversation that his code is licenced with AGPL
which is included with this software

This package was mainly designed after the **pcommerce.payment.saferpay** plugin, and works almost identically, except ofcourse this uses a different payment platform.

Installation instructions
-------------------------

*Step 1 - installing*
*********************

Install via the plone quickinstaller

*Step 2 - configure plone*
**************************

Look at the docdata settings in the site configuration

You should set the docdata specific settings and these should obviously
match the settings as you have configured them with Docdata.

- `DocData merchant name`
- `DocData merchant password`
- `DocData profile`
- `DocData debug mode`

*step 3 - Docdata settings*
*************************

In Docdata there are a couple of settings which you should set:

return URL (in your merchant profile -> URLs)

  http://my.website.com/processDocdata?form_id=

note that the form_id is necessary. This should really be the 'orderId'
but since I had some non related integration issues I changed it to form_id
docdata will automatically add the order_id to last GET parameter

Docdata should be able to access this URL in order for it to work.

*LICENCE*
*********

This code is open source. It's licenced under the AGPLV3 licence, which is compatible with the GPLV3 
See LICENCE.txt
