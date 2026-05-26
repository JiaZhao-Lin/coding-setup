
## ROOT Setup
This allow import ROOT in venv
	
	echo 'source $(brew --prefix root)/bin/thisroot.sh' >> .venv/bin/activate

## Python
	pip3 install --upgrade pip
	pip3 install isort
	pip3 install notebook
	pip3 install pandas
	pip3 install matplotlib
	pip3 install uncertainties
	pip3 install uproot
	pip3 install tqdm
	pip3 install mplhep
	pip3 install lhcbstyle

	pip3 install pdg
	pip3 install dask
	pip3 install "dask[distributed]"
	pip3 install scikit-learn
	pip3 install tensorflow
	pip3 install hepdata_lib

	pip3 freeze | awk -F'==' '{print $1}' | xargs -n 1 pip3 install -U

## Terminal
	brew unlink python@3.14 && brew link python@3.14


## Clean Hash
Every time you run a command (like python3, git, ls), the shell searches your $PATH directories to find the corresponding executable.
To avoid doing this lookup every single time, the shell keeps a hash table
(r for reset) clears that hash table

	hash -r


## Link
	ln -s ../.rootlogon.py ./
	ln -s ../common.py ./

## Github
1. Set for only the current repo:

		git config user.name "Your Name"
		git config user.email "you@example.com"

1. Check current repo:

		git config --local user.name
		git config --local user.email

1. Set globally:

		git config --global user.name "Your Name"
		git config --global user.email "you@example.com"

1. Check globally:

		git config --global user.name
		git config --global user.email