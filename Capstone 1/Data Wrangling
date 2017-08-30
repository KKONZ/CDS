Capstone Project 1 data wrangling.

The data set for my project uses .mid files downloaded from the "Kunst Der Fuge" website, http://kunstderfuge.com/.
This work is a continuation of the paper that was released by Sony CSL for Deep Bach. My project will start with applying the same modeling techniques to new data.
The original project from Sony was trained on Bach Chorales that are included in the Music21 Python library.
For my project I wanted to explore using String Quartetes instead of Bach Chorales. There are a number of issues that need to be resolved
in order to acquire and clean the data to create this type of model.
The first step is to download the data. To do this in a dynamic way I chose to use Selenium to authenticate into the web service, walk through the 
site and download the relevant data files.
Once the data was downloaded the files need to be parsed by the Music21 library and chopped up into smaller segments to reduce the amount of noise in
the models. The Bach pieces in general are much shorter in duration than the quartets so to increase the corpus size and to reduce the noise from having
too large of training files, the original files have been broken into 20 measure and modulus files to be trained on.
Next the midi files metadata needs to be cleaned as well. There were a number of files that had multiple instruments (2 piano staffs in the metadata) 
for a single voice. The insturment elements are simply removed.
There are additional errors in the training data that still need to be addressed. Hopefully this will be a similar process to stripping the insturments.
The documentation indicates that the voices need to be monophonic per line but the Bach files are not all monophonic per line. Perhaps adding logic
to remove all but 1 note per line when there are chords will result in files that can be transformed with the script in the Deep Bach open source repository.
