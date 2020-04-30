## APP: Fast Style Transfer:

1. GitHub repo: https://github.com/lengstrom/fast-style-transfer

2. video: https://www.youtube.com/watch?v=xVJwwWQlQ1o

3. packages install:

Run:
```shell
conda create -n style-transfer python=3
conda activate style-transfer
conda install tensorflow scipy pillow
pip install moviepy
pip install imageio==2.4.1
	
(may need to restart the terminal and run `conda activate style-transfer`, then run...)
python -c "import imageio; imageio.plugins.ffmpeg.download()"
```

So far, the environment has been set.

Evaluation:
	
1) Rain Princess checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/rain-princess.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/rain-princess-labrador.jpg
```
2) La Muse checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/la-muse.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/la-muse-labrador.jpg
```

3) Udnie checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/udnie.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/udnie-labrador.jpg
```
		
4) Scream checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/scream.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/scream-labrador.jpg
```

5) Wave checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/wave.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/wave-labrador.jpg
```

6) Wreck checkpoint
```shell
python evaluate.py --checkpoint ./checkpoint/wreck.ckpt --in-path ./test-images/Labrador.jpg --out-path ./test-results/wreck-labrador.jpg
```

4. packages:

	1) pillow: an image processing library
	
	2) ffmpeg: an application converting images and videos


5. Trouble-shooting:

	1) get error 
		RuntimeError: imageio.ffmpeg.download() has been deprecated. Use 'pip install imageio-ffmpeg' instead.'
	   when running 
	   	```python -c "import imageio; imageio.plugins.ffmpeg.download()"```

	   solution:		
	   run ```pip install imageio==2.4.1``` before and restart the terminal and reactivate the environment as mentioned above.

	   Ref: https://github.com/artyshko/smd/issues/3
	
	2) get error
		AttributeError: module 'scipy.misc' has no attribute 'imread'
	   when evaluating

	   solution:
	   need to downgrade package version
	   
	   scipy -> 1.1.0: run ```conda install scipy=1.1.0```
	   
	   tensorflow -> 1.15.0: run 
		```
	   	conda uninstall tensorflow
	   	conda install -c conda-forge tensorflow=1.15.0
	   	```

	   Refs:
	   https://stackoverflow.com/questions/15345790/scipy-misc-module-has-no-attribute-imread
	   https://github.com/tensorflow/tensorflow/issues/31077


6. Citation:
```
@misc{engstrom2016faststyletransfer,
    author = {Logan Engstrom},
    title = {Fast Style Transfer},
    year = {2016},
    howpublished = {\url{https://github.com/lengstrom/fast-style-transfer/}},
    note = {commit xxxxxxx}
  }
```
