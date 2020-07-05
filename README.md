# CS224u: Natural Language Understanding

Code for [the Stanford course](http://web.stanford.edu/class/cs224u/). The code is written to run under Python 3.7; [setup.ipynb](setup.ipynb) provides  additional details.

# Instructors

* [Bill MacCartney](http://nlp.stanford.edu/~wcmac/)
* [Christopher Potts](http://web.stanford.edu/~cgpotts/)

# Set up on Google Colab

[Google Colab](https://colab.research.google.com/notebooks/intro.ipynb) is a way to run code on Google VMs (not using resources of your machine), which prevents any setup shenanigans for all machine learning packages like TensorFlow or PyTorch.

Colab offers runtime options where we can choose between None, GPU and TPU.

Colab works seamlessly with [Google Drive](https://drive.google.com/drive/u/0/my-drive). We can also upload any directory onto the workspace of Colab or work directly with S3.

- For linking to Google Drive (this step will ask for auth creds)
```bash
from google.colab import drive
drive.mount('/content/drive')
```
- Cloning repo into workspace
```bash
!git clone https://github.com/cgpotts/cs224u.git
```
this gets the full git dir in /content/cs224u
- To be able to import python packages from the cloned repo dir
```bash
import sys
sys.path.append('/content/cs224u')
```
after this we can import anything from the github repo and work with data like shown in [sample notebook](https://nbviewer.jupyter.org/github/cgpotts/cs224u/blob/master/vsm_01_distributional.ipynb)
- All normal commands like !ls, !cp, !pwd work as expected

- WordNet
```bash
import nltk
nltk.download('wordnet')
```
Then can use any command with wn.lemmas(xxx)
