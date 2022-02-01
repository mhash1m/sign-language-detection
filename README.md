# sign-language-detection

A Sign Language detection project using Mediapipe landmark detection and Tensorflow LSTM.
The project is built for a vocabulary of 3 words, but more can be added by collecting and adding data for other words.

## Vocabulary

- Open
- to
- Work


## Output

![](output.gif)

### Disclaimer

Colab doesn't detect webcam and you can't use it for mediapipe detection and dataset collection through webcam so most of that was done locally and then training and inference using Tensorflow was performed on Colab.

You can uncomment the commented part if you wish to do all that locally.
In my case, I had some clash between mediapipe and tensorflow on the ARM architecture m1 mac.

The notebook uses the [approach to Sign Language Detection](https://www.youtube.com/watch?v=doDUihpj6ro&t=7087s) by Nicholas Renotte, of course with a whole bunch of tweaks to suit my usecase 🙂

## Tweaks:
- Input and output in the form of videos to work with colab.
- Remove face landmarks as they end up just being noise.
- Use tanh activation as it works way better with LSTMs compared to relu.
- Colors and Cosmetics.
- Disclaimer at bottom.
- Different threshold value for inference.
