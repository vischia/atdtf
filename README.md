# Aplicaciones y Tratamiento de Datos en Tecnología y Física, 2024-2025 and following years
    
(c) Pietro Vischia (pietro.vischia@cern.ch)


## Tutorial organization

Ideally you would be running the tutorial on your laptop, following the instructions and explanations given by me in the big screen in the room.
If, for any reason, you cannot run the tutorial, you are welcome to just watch the tutorial steps being executed in the big screen by me.

## How to run the tutorial on your local machine

#### 1. Check out the code
```
git clone git@github.com:vischia/atdtf.git
cd atdtf/
```
or
```
git clone https://github.com/vischia/atdtf.git
cd atdtf/
```

#### 2. Create a python environment and install requirements (follow one of the options 2.1, 2.2, or 2.3)

If your laptop can run ML models without too much hassle and you have some (approximately 5 GB) free disk space, follow the instructions in `2.1` or `2.2`. Otherwise, I suggest running on Colab by following the instructions in `2.3`.
    
##### 2.1 Using conda

```
conda create --name atdtf python==3.10
conda activate atdtf
conda install --file requirements.txt -c conda-forge -c pytorch -c nvidia -c scikit-learn
pip install livelossplot
```

To deactivate the environment, you should run `conda deactivate` from the command prompt.

##### 2.2 Using virtualenv

```
virtualenv -p python3.10 atdtf
source atdtf/bin/activate
pip install -r requirements_venv.txt
```

To deactivate the environment, you should run `deactivate` from the command prompt.

##### 2.3 Using Google Colab (google account needed)

Go to [Google Colab](https://colab.research.google.com/), select `GitHub` as a source, and fill in the path to this repository (`https://github.com/vischia/atdtf`). Possibly Google will ask for access to your GitHub account, although installing from a public third party repository should not require that, in principle.

When the colab instance is active, open the jupyter notebook you want to access (e.g. `01_dataChallenge.ipynb` and run the cell labelled "*If you are using COLAB*"

Note that, to have persistency of the files and changes, and to be able to push back the repository, you should use the first cells in the notebooks to load your google drive account.

*While we can provide some limited help, it is expected that you set up your workflow in Colab independently.*

#### 3. Run the tutorial

For local environments, run

```
jupyter notebook
```

and open a notebook, for instance `lesson_1.ipynb`, in the browser window that is opened.

From Colab, open `lesson_1.ipynb`.

If you prefer to run a regular python script, you can convert the notebook using the command:

```
jupyter nbconvert --to script lesson_1.ipynb
```

This will create a file `lesson_1.py` that you can pass as a command line argument to the python interpreter.
You may have to add a few `plt.show()` or `plt.savefig()` to the code here and there, to visualize/save outputs, though.
