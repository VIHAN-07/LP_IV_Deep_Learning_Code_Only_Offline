# Deep Learning Practical Notebooks

20 small, independent TensorFlow/Keras and CBOW notebooks for LP IV practicals.
The examples use direct steps without custom functions or classes.

| Folder | Practicals |
| --- | --- |
| [01_FNN](01_FNN) | MNIST, Fashion-MNIST, CIFAR10 and Sign Language FNNs |
| [02_CNN](02_CNN) | CIFAR10, MNIST and Sign Language CNNs |
| [03_Autoencoder](03_Autoencoder) | Credit-card fraud, ECG, smart-grid, NASA and Sign Language anomalies |
| [04_CBOW](04_CBOW) | Document classification, Twitter, word similarity and recommendations |
| [05_Transfer_Learning](05_Transfer_Learning) | VGG16 classification, fine-tuning and prediction plots |

## Run

```powershell
python -m pip install -r requirements.txt
python -m jupyter lab
```

Open a notebook and run its cells from top to bottom. Its working directory
must be the exercise folder containing that notebook.

## Datasets

**Datasets and pretrained weights are not included in this repository.**
Put the required CSV/text files beside the notebooks in each exercise folder.
Transfer-learning image folders and the local VGG16 weights belong inside
`05_Transfer_Learning/`.

See [EXAM_DATASET_MAPPING.txt](EXAM_DATASET_MAPPING.txt) for exact filenames and
folder names. Once the dependencies, data and weights are available locally,
the notebooks do not download anything during execution.

The Git ignore rules allow only the notebooks and setup documentation.
Datasets, model weights, training artifacts, backups and archives stay local.
Generated validation reports and prediction figures also remain local.

## Assignment notes

- 3B and 3E retain the agreed ECG replacements for their original statements.
- 1B follows the Fashion-MNIST title despite the CIFAR10 typo in its substep.
- Section 5 performs image classification, including actual CNN fine-tuning;
  it does not train a bounding-box detector.
- Short real-data checks were run for the assignment updates. These are not
  full-training accuracy benchmarks, and no target accuracy is guaranteed.

See [STATEMENT_COVERAGE.txt](STATEMENT_COVERAGE.txt) for the requirement mapping
and [README.txt](README.txt) for detailed notebook patterns.
