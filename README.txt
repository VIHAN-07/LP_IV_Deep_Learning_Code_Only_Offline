EXAM NOTEBOOKS - SHORT VERSIONS

Run the cells from top to bottom, inside the notebook's folder.
Datasets and VGG16 weights stay beside the notebooks; nothing downloads.
No def, lambda, custom classes, callbacks or extra validation stages.

1: read CSVs -> separate labels -> divide pixels by 255 -> FNN -> fit -> evaluate -> plots.
   1A uses SGD and 11 epochs. 1B uses SGD. 1C/1E use Adam.
2: the same image data -> reshape -> one convolution -> pool -> classify -> evaluate.
3: normal training data -> autoencoder -> reconstruction error -> threshold -> anomalies.
   3C/3D retain the required LSTM time windows. 3F excludes class 24 from training.
4: preprocess words -> CBOW -> similar words, classification or recommendations.
   4A includes stop-word removal and padding. 4D ranks cosine similarity.
5: load image folders -> freeze VGG16 -> train -> unfreeze top layers -> fine-tune -> evaluate -> show prediction.

3B/3E retain the agreed ECG replacements. 1B follows the Fashion-MNIST title.
Section 5 is image classification, as interpreted from the supplied datasets.
See EXAM_DATASET_MAPPING.txt for filenames and STATEMENT_COVERAGE.txt for the steps.
Small training checks are recorded in SIMPLE_CODE_VALIDATION.json.
These are simple demonstration models; earlier accuracy scores do not apply.
EXAM_CODE_ONLY.zip contains code/docs only. Datasets and weights are not zipped.
