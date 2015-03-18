# s3-bash #
Amazon's S3 is an original service. Many people use it - but until now it's needed knowledge of a programming language to use it.

s3-bash is a small collection of BASH scripts to let you use it from an Unix, Linux or Mac OS X command line without needing Perl, Python, Java, .Net, etc...

# IMPORTANT #
I can no longer actively maintain s3-bash due to other commitments on [StormMQ](http://stormmq.com). If you'd like to take over running of it, please drop me an email or raise an issue.

### Using It ###
_Just unpack the tar!_

  * To get files: use `./s3-get`
  * To put files: use `./s3-put`
  * To delete files: use `./s3-delete`

All of these programs take **-h** for help.

### Dependencies ###
If you're using Linux or Cygwin, you will need to have _gnu coreutils_ (_textutils_ as was), _curl_ and _OpenSSL_ installed. These are pretty standard on most modern distributions.

If you're using a Mac, we've only tested this on Mac OX X Tiger.

We've made some changes in 0.01 so that it now works irrespective of your locale and does basic checking for corrupt secret keys.

### Notes ###
  * Amazon custom headers are not completely supported yet.
  * Temporary files are not properly cleaned up (`/tmp/s3-*`). These can be deleted by hand.
  * The Amazon custom date header is not supported as it is not needed.
  * The format of the custom header file is header: value. We do no support repeated headers or long headers folded on to a new line (rarely encountered).

### Coooool ###
_(Well, we think it is)_
The bash code in `s3-common-functions` implements the HMAC part of HMAC-SHA1 in pure bash...