Return a list of related pages between two pdfs.

##### Requirements

* Ubuntu >= 14.10 
* Python 2.7

##### Install

Run as sudo

```
apt-get install python-pythonmagick libpq-dev python-dev libopencv-dev python-opencv pdftk 

pip install pyPdf

ln /dev/null /dev/raw1394 # disable libdc1394 error (cause by unused opencv coedec )

python setup.py test
```

Make sure pdfs are decompressed before running script

```pdftk doc.pdf output doc.unc.pdf uncompress```


Tests

``python2.7 inspection/test.py``
##### Example Usage

``ox_inspect -h``

``ox_inspect data/test/A.pdf data/test/B.pdf``

``ox_inspect --cases example --include Example1 data/test/A.pdf data/test/F.pdf``

``ox_inspect --cases example --include Example2 --exclude DefaultTest data/test/A.pdf data/test/F.pdf``

``ox_inspect --cases example --include Example3 --exclude DefaultTest --check any data/test/A.pdf data/test/F.pdf``

``ox_inspect --cases example --include Example1 --check any  data/test/m25.pdf  data/test/m26.pdf ``

##### Algorithms

http://docs.scipy.org/doc/numpy-1.10.0/reference/generated/numpy.array_equiv.html#numpy.array_equiv

http://docs.opencv.org/2.4/modules/imgproc/doc/histograms.html?highlight=comparehist#comparehist

https://en.wikipedia.org/wiki/Longest_common_subsequence_problem

##### Python Modules

https://docs.python.org/2/library/unittest.html

