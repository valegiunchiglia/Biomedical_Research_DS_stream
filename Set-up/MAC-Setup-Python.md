# Installing software on a Mac

## Step 1: Download Homebrew

1. Go to https://brew.sh/ and copy the command under `Install Homebrew`. The command should look like this (but check that it didn't change)

   `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Open a terminal by pressing  `Command + Space ` and typing  `terminal `, or by selecting the Terminal icon from the Launchpad (might be inside a folder called "Others")
3. Paste the command into the terminal and press  `Enter `
4. Enter your password or press `Enter` whenever asked
5. Once the initial download is done, make sure to follow the last steps, especially the ones that mention "adding Homebrew to your PATH"

## Step 2: Download Anaconda
1. Go to this link https://www.anaconda.com/products/distribution
2. Press on `Download` under `Anaconda Distribution`
3. When the download is completed, open the .pkg file (the file requires more or less 600MB of space)
4. A window should pop up: follow the instructions and install Anaconda

## Step 3: Set up a conda environment
1. Open a terminal by pressing  `Command + Space ` and typing  `terminal `, or by selecting the Terminal icon from the Launchpad (might be inside a folder called `Others`)
2. Write the following command in the terminal and press  `Enter ` 
   
   `conda create -n WorkshopsDS python=3.9 ipykernel`

3. Reply `yes` or `y` when asked and press  `Enter `
4. Activate the conda environment by pasting the following command in the terminal and by pressing  `Enter `

    `conda activate WorkshopsDS`

    To understand if you were succesfull, at the beginning of the terminal line where you are writing you should see (WorkshopsDS) instead of (base)
5. Copy the following command in the terminal and press `Enter`

    `python3 -m ipykernel install --user --name python3_WorkshopsDS --display-name "Python3.9 (WorkshopsDS)"`

## Step 4: Download the modules of interest
1. Open a terminal by pressing  `Command + Space ` and typing  `terminal `, or by selecting the Terminal icon from the Launchpad (might be inside a folder called `Others`)
2. Activate the environment by pasting this command in the terminal and pressing `Enter`.
   
   `conda activate WorkshopsDS`
3. Install the modules of interest by pasting this command in the terminal and pressing  `Enter`.

    `conda install numpy pandas matplotlib seaborn sklearn`
    
    Reply `yes` or `y` when asked and press  `Enter `

    
## Step 5: Download the lectures material and start a Jupyter
2. Open a terminal by pressing  `Command + Space ` and typing  `terminal `, or by selecting the Terminal icon from the Launchpad (might be inside a folder called `Others`)
3. Copy the following commands and press  `Enter ` at the end of each command

     `cd`

     `cd Desktop/`

     `git clone https://github.com/valegiunchiglia/Biomedical_Research_DS_stream.git`

     `cd Biomedical_Research_DS_stream`

    `jupyter lab`

    In order to be able to run the command correctly you should not be in your conda environment. This means that at the beginning of the line where you are writing, you should see (base). If you don't see (base) but (WorkshopsDS), then write the following command, press `Enter` and repeat step 3.

    `conda deactivate`

4. If the command worked correctly, a webpage should be opened automatically with a jupyter lab page. 

## Extra resources

If you have never used Jupyter Notebook before, it might be useful going through this tutorial. This will teach you about its functionalities.

https://www.dataquest.io/blog/jupyter-notebook-tutorial/



