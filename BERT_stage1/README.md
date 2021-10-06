# BERT_Chinese_Emotion_Classification
An implementation for "No more fear: the long-term impacts of air pollution on social media emotions in 160 Chinese cities"

### Installation
Install TensorFlow following the instuctions on the [official website] (https://www.tensorflow.org/). The code has been tested over TensorFlow 1.11.0.
Before running, you need to download Google's pre-trained model chinese_L-12_H-768_A-12 (https://github.com/google-research/bert). For Chinese, the specific parameters of Google's BERT pre-training model are as follows:
```
Chinese Simplified and Traditional, 12-layer, 768-hidden, 12-heads, 110M parameters
```

### Train run
```
python3 run_classifier.py or sh train.sh
```

### Emotion classification run
```
python3 run_classifier_json.py
```

Functions get_test_examples and get_test_examples_json are used to process TXT and JSON files, respectively. See predict_texts.txt and Weibo2014_sample.json in the data directory for the input file format, and the output file is out_emotionlabels.txt in sim_model/class_mood_try/.

The task has two emotional labels, as shown in the function get_labels:
```
    def get_labels(self):
        return ['-1', '0']  #-1: nonemotional label, 0: emotional label
```

### Acknowledgement
We would like to acknowledge the following repositories for allowing us to use the official versions of the BERT and some helper functions implemented in this paper:
1. https://github.com/google-research/bert
2. https://github.com/renxingkai/BERT_Chinese_Classification
