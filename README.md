# Drupal Patch for nG Firewall

This repo contains a patch file for adding the [Perishable Press nG
Firewall](https://perishablepress.com/nG-firewall/) and [nG
Addon](https://perishablepress.com/stop-aggressive-scanning-uploads/) to
Drupal.

All credit for the nG Firewall rules goes to Perishable Press and
whomever they list as contributors.

I don't vouch for the utility or functionality of the firewall rules on
a Drupal site. I've used it for years on my site without any
issues with the exception of an edit to allow access to files under the 
`system` directory. Thanks to the folks at Perishable Press, that change 
was added to newer versions of the firewall.

## Usage

Since this is a _patch file_, use it to _patch_ `.htaccess`.

There are several ways to do this. For sites using the standard Drupal
composer setup with Drupal `^8.8.x`, you can use the standard patching
mechanism in `composer.json`.

### Example

```json
{
  ... everything else in composer.json ...
  "extra": {
    "patches": {
      "drupal/core": {
        "htaccess nG Firewall": "https://raw.githubusercontent.com/kentr/drupal-nG-firewall-patch/master/htaccess-nG-firewall.patch"
      }
    }
  }
}
```

See [this post](https://kentrichards.net/blog/patching-drupal-scaffold-files-composer-patches) for more information.

## Contributing

If you have suggestions for the firewall itself, go to [Perishable Press](https://perishablepress.com/nG-firewall/).

If you have suggestions for the patch file or the instructions in this
repo, create a PR here. However, please note that this repo is minimally-maintained.
