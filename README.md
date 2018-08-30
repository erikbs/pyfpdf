What is this?
-------------

Slightly modified version of [pyfpdf](https://github.com/reingart/pyfpdf) (FPDF
for Python) v. 1.7.2 (30 Aug 2018) that supports a few features I needed in a
private project, most importantly the ability to add images without having to
use temporary files. This fork will not be maintained and I set the version
number to 1.7.2m to avoid confusion with the one that is actively developed.

Why not just submit a pull request? There is already a major rewrite, v. 2.0.0,
but my project relies on v. 1.7.2. In addition, pull requests to 1.7.2 have not
been reviewed in several months.

Differences
-----------

* 1.7.2 supports reading from files or http(s):// URLs. 1.7.2m also supports data URIs and in-memory streams (like io.BytesIO).
* 1.7.2 implements GIF support by conversion to PNG using a temporary file. 1.7.2m uses io.BytesIO to convert files in-memory instead.
* 1.7.2 supports PNG, GIF (through PIL) and JPEG image files. PIL also provides TIFF/JPEG2000 support, but files in those formats will be interpreted as mislabeled GIFs. 1.7.2m knows these formats, files are converted to PNG right away instead of being passed to the JPEG parser first.

Installation
------------

```
   git clone https://github.com/erikbs/pyfpdf.git
   cd pyfpdf
   python setup.py install
```

Prerequisites
-------------
The [Python Imaging Library](http://www.pythonware.com/products/pil/) 
(PIL) is needed for GIF/TIFF/JPEG2000 support. For Python 3, 
[Pillow - The friendly PIL fork](https://github.com/python-pillow/Pillow) is 
supported.

Documentation
-------------
See [https://github.com/reingart/pyfpdf](https://github.com/reingart/pyfpdf).
