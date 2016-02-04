===========
Description
===========

``geolang`` is Simple Georgian Language ToolKit for Python 3

Installation Requirements
-----------------------------------

* Python 3.0, 3.1, 3.2, 3.3, 3.4, 3.5
* Django >= 1.7 
* To install the source, download it from https://github.com/Lh4cKg/simple-geolang-toolkit and do ``python setup.py install``.

To install ``geolang``::

    $ git clone https://github.com/Lh4cKg/simple-geolang-toolkit "geolang"
    $ cd geolang
    $ sudo python setup.py install # if you do not have a default Python 3, then use the python3 install instead of python install

Usage
---------

To use ``geolang``, just import it in your project like so:

>>> import geolang as _ka

You can convert the Latin words in Georgian

>>> latin_to_ka = _ka._2KA
>>> _text_2ka = "i love you python and django"
>>> latin_to_ka(_text_2ka)
ი ლოვე  ყოუ  პყტჰონ  ანდ  დჯანგო

You can convert the Georgian words in Latin

>>> ka_to_latin = _ka._2LAT
>>> _text_2lat = "მე მიყვარს ანი"
>>> ka_to_latin(_text_2lat)
me miyvars ani

>>> encode_slugify = _ka.encode_slugify
>>> _try_encode_slugify = "ი ლოვე ყოუ პყტჰონ ანდ დჯანგო"
>>> encode_slugify(_try_encode_slugify)
b'i-love-you-python-and-django'
>>> encode_slugify(_try_encode_slugify, _slugify=False)
b'i love you python and django'
>>> _try_encode_slugify_1 = "é\jcàé\jcàétéétéé\jéé\jcàété\jcàétécàété"
>>> encode_slugify(_try_encode_slugify_1)
b'ejcaejcaeteeteejeejcaetejcaetecaete'

Source Code
-----------------
The source code can be found on github_.

Contributing
-----------------
There are plenty of ways to contribute to this project. If you think you’ve found a bug please submit an issue.


.. _github: https://github.com/Lh4cKg/simple-geolang-toolkit