<!-- 1. Open WSL and cd to this folder 
cd /mnt/c/Users/ellia/OneDrive/Desktop/NUS_FYP_github/eenets_pytorch_et/ -->

THE BELOW DOES NOT WORK. 
<!-- 2. Can't run your program until you set up the requirements but it is an externally managed environment
3. Make a venv
sudo apt update
sudo apt install python3-venv

python3 -m venv venv
source venv/bin/activate

4. Get the requirements installed in the venv 
pip install -r requirements.txt
(still does not work)

5. Install the requirements individually in venv
apt install python3-scipy
apt install python3-six
apt install python3-pandas
apt install python3-numpy
apt install python3-matplotlib


6. run the python command (see the README)
TEST
$  -->
error: externally-managed-environment


<!-- - NEED TO INSTALL THE PACKAGES MANUALLY OUTSIDE IN WSL.  -->




python main.py --model eenet18 --dataset cifar10 --num-ee 2 --epochs 10
<!-- source venv/bin/activate -->

<!-- END. deactivate virtual env  -->



1. IN VSCODE PS terminal, create a venv
python -m venv venv2
2. Activate 
.\venv2\Scripts\Activate

3. Install libraries
pip install torch
pip install six
pip install scipy
pip install pandas
pip install numpy
pip install matplotlib

pip install torchvision
4. try
python main.py --model eenet18 --dataset cifar10 --num-ee 2 --epochs 10
