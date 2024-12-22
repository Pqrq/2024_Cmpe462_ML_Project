# How to Run the Model

Option 1: Using Jupyter Notebok

* Download "AllModels.ipynb" and "balanced_data_3.csv" into the same folder
* Open Jupyter Notebook inside that folder
* Run the blocks inside AllModels.ipynb in the given order

Option 2: Using Google Colab (recommended)

* Open AllModels.ipynb code inside Google Colab
* At the left side of the screen, there is a folder icon
* Click on that icon. There should be only the "sample_data" folder under tha title "Files"
* Add "balanced_data_3.csv" directly under the "Files" title (not inside "sample_data")
* Run the blocks inside AllModels.ipynb in the given order

# About Reproducibility

Note that inside our model, our only source of randomness is at "split_dataset()" function.
Inside this function, we have the lines "
    seed = 462
    random.seed(seed)
    np.random.seed(seed)
    torch.manual_seed(seed)
    torch.cuda.manual_seed(seed)
    torch.backends.cudnn.deterministic = True
    torch.backends.cudnn.benchmark = False
", which sets the seed to a constant, providing reproducibliity of our results.
