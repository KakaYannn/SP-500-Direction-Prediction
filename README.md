How to Run This Notebook

Follow these steps to run the pipeline:

1. Install the required dependencies:
   ```
   pip3 install -r requirements.txt
   ```
   (Or use `python3 -m pip install -r requirements.txt` if `pip3` is not available.)

2. Open the `COMP90051_Project_NEW.ipynb` notebook in VS Code or JupyterLab.

3. Execute the notebook cells sequentially according to the pipeline:
   - **Section 1:** Environment setup (necessary imports and random seeds)
   - **Section 2:** Download and clean the stock data, build features and the target variable
   - **Section 3 (Optional):** Systematic feature selection (feature selection pipeline). You may skip directly to Section 4 if you want to use the default features.
   - **Section 4:** Create train/test splits and generate `datasets_split` for subsequent training

4. For model training, run the corresponding cells for each model and feature set combination (e.g., Logistic Regression, Random Forest, FT-Transformer using Baseline_5, RF_MDA_20, or All_Features). Each training cell provides a progress bar and saves its results to `all_results`.

5. View aggregated results and confusion matrices in the final sections of the notebook.

The pipeline uses temporal splits to prevent data leakage. Progress during long training runs is displayed using `tqdm`.
