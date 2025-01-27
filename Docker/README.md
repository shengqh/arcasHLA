# Container for arcasHLA #

Installs up-to-date versions of arcasHLA and all dependencies:

- arcasHLA
- coreutils
- [Samtools v1.19](http://www.htslib.org/)
- [bedtools v2.29.1](http://bedtools.readthedocs.io/)
- [pigz v2.3.1](https://zlib.net/pigz/)
- [Kallisto v0.44.0](https://pachterlab.github.io/kallisto/)
- Python 3.6
- [Biopython](https://biopython.org/wiki/Download)
- NumPy
- SciPy
- Pandas

### Build ###
In order to use this arcasHLA container, install Docker and build in this directory:
```
docker build -t <image_name> .
```
### Run ###
Interactively ("image_name" is as above):
```
docker run -it --entrypoint bash -v <path/to/files>:<docker/path/to/files> <image_name>
```
Noninteractively ("image_name" is as above), e.g. 'arcasHLA extract':
```
docker run \
	--rm -v <path/to/files>:<docker/path/to/files> \
	<image_name> \
	arcasHLA extract --o docker/path/to/files/out_dir \
	[other options] docker/path/to/files/sample.bam & 

```
