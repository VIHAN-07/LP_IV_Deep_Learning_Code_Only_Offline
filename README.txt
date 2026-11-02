SIMPLE OFFLINE EXAM NOTEBOOKS - NO CUSTOM FUNCTIONS

All 20 notebooks contain code cells only and run independently.
Run the cells from top to bottom. No helper scripts need to be run.
No notebook defines functions, lambdas or custom classes.

Run each notebook from its exercise folder. CSV/text files are beside the
notebooks, so paths are direct filenames such as "mnist_train.csv".
Each exercise folder contains its own required datasets:
  01_FNN/                  FNN CSV files
  02_CNN/                  CNN CSV files
  03_Autoencoder/          autoencoder CSV files
  04_CBOW/                 CSV files and document3.txt
  05_Transfer_Learning/    caltech101/, intel/, fashion_mnist/, VGG16 weights
Shared datasets are independent copies in each section that uses them.
No external dataset folder or parent-folder path is needed.
Install requirements.txt beforehand. All data and VGG16 weights load locally.

EXAM_CODE_ONLY.zip contains notebooks and documentation only; it excludes data.
Datasets and VGG16 weights stay in the exercise folders and are not zipped.
The historical root data/ folder and external originals are retained for
reference. Current notebooks do not use them.

LEARN ONE PATTERN PER SECTION
1A, 1B, 1C, 1E: imports -> CSVs -> scale -> dense model -> fit -> evaluate -> plots.
All four use the same Dense(256), Dense(128), Dropout(0.2) architecture.
Dataset names, input/output sizes and required optimizer/epochs differ.
1A keeps SGD with 11 epochs; 1B keeps SGD. Others use Adam.
Sign Language needs three extra lines to encode its nonconsecutive labels.
CIFAR needs a train/test split because the exam supplies only one CSV.
Loss and accuracy plots use one pandas plotting command.
Section 1 has 19 nonempty code lines per notebook, or 22 for Sign Language.
pop("label") extracts labels by name; the remaining columns are image pixels.
Loading and label extraction share a cell so that it can be rerun safely.

2A, 2B, 2C: the same two-convolution CNN, training, evaluation and plot pattern.
CIFAR's channel-first CSV pixels require a different reshape from grayscale.

3A, 3B, 3E, 3F: normal data -> autoencoder -> reconstruction error -> threshold.
3A compiles with Adam, MSE loss and an explicit MAE reconstruction metric;
fraud accuracy uses thresholded errors; AUC uses the reconstruction scores.
3B and 3E are identical approved ECG replacements. ECG has no CSV header;
label 1 is normal and 0 abnormal. 3C and 3D retain required LSTM time windows;
energy splits stay chronological and NASA splits use separate engines.

4A-4D: tokenize -> CBOW Word2Vec -> classification/similarity/recommendation.
4A removes HTML and stop words, while retaining no/not/never for sentiment.
Its vocabulary and CBOW embeddings use training documents only. Word IDs are
padded to one training-derived length (at most 300). A frozen embedding layer
and masked mean ignore padding, then feed a dense classifier. Loss and accuracy
are evaluated on the held-out test set.

5A-5C: class files -> disjoint splits -> frozen VGG16 features -> dense head.
The head trains for 40 epochs on cached, normalized features. The full model
then combines VGG16, feature normalization and that head. It unfreezes only
the top two convolution layers, recompiles with Adam at 0.00001, and fine-tunes
for one raw-image epoch. Final loss/accuracy and an actual/predicted image plot
complete the example. Head training is fast; raw-image fine-tuning takes longer.
Caltech keeps all 101 classes, excludes background, uses 30 training-pool images
per class (24 fit, 6 validation), and up to 10 separate test images per class.
Fashion excludes the extra nested train folder. RGB images load in small batches.
VGG16 images, features and labels are written out for each split directly.
Time-series windows use ordinary loops, with no function definitions.

No exception handling, download logic, training callbacks or augmentation layers.
Dataset-specific steps remain where needed for correct practicals.
1B follows its Fashion-MNIST title; the CIFAR10 mention in its substep is a typo.
Section 5 follows the image-classification interpretation of the statements:
the supplied datasets have class folders, not bounding-box annotations.
STATEMENT_COVERAGE.txt maps the 18 required exercises and the 3B/3E exceptions.
EXAM_DATASET_MAPPING.txt lists every notebook's local files.
See SIMPLE_CODE_VALIDATION.json and EXAM_DATASET_VALIDATION.json for the scope
and results of validation. Short execution checks are not full-training accuracy
measurements; earlier benchmark figures belong to their original versions.
No target accuracy is promised.
