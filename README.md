# Microsoft Speech API: Android Speech-to-Text Client Library and Samples

This repo contains the Android client library and samples for Speech-to-Text in Microsoft Speech API, an offering within [Microsoft Cognitive Services on Azure](https://azure.microsoft.com/en-us/services/cognitive-services/), formerly known as Project Oxford.

* [Learn about the Speech API](https://azure.microsoft.com/en-us/services/cognitive-services/speech/)
* [Read the documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/speech/home)
* [Find more SDKs & Samples](https://www.microsoft.com/cognitive-services/en-us/SDK-Sample?api=bing%20speech)

## The Client Library

The Speech To Text client library is a client library for Microsoft Speech, Speech-to-text API.

The easiest way to consume the client library is to add the `com.microsoft.projectoxford:speechrecognition` package from Maven Central Repository. To find the latest version of client library, go to http://search.maven.org, and search for "g:com.microsoft.projectoxford".

To add the client library dependency from build.gradle file, add the following line in dependencies.

```
dependencies {
    //
    // Use the following line to include client library from Maven Central Repository
    // Change the version number from the search.maven.org result
    //
    compile 'com.microsoft.projectoxford:speechrecognition:1.2.2'

    // Your other Dependencies...
}
```

To add the client library dependency from Android Studio:

1. From Menu, Choose `File` \> `Project Structure`.
2. Click on your app module.
3. Click on `Dependencies` tab.
4. Click "+" sign to add new dependency.
5. Pick `Library dependency` from the drop-down list.
6. Type `com.microsoft.projectoxford` and hit the search icon from `Choose Library Dependency` dialog.
7. Pick the client library that you intend to use.
8. Click `OK` to add the new dependency.
9. Download the appropriate JNI library `libandroid_platform.so` from [this page](https://github.com/Microsoft/Cognitive-Speech-STT-Android/tree/master/SpeechSDK/libs) and put into your project's directory `app/src/main/jniLibs/armeabi/` or `app/src/main/jniLibs/x86/`.

## The Sample

This sample demonstrates the following features using a wav file or external microphone input:

* Short-form recognition
* Long-form dictation
* Recognition with intent

### Requirements

* Android OS must be Android 4.1 or higher (API Level 16 or higher)
* The speech client library contains native code. To use this sample in an emulator, make sure that your build variant matches the architecture (x86 or arm) of your emulator.

### Build the sample

1. First, you must obtain a Speech API subscription key by following the instructions on [Subscriptions](https://azure.microsoft.com/en-us/try/cognitive-services/).

2. Start Android Studio, choose `Import project (Eclipse ADT, Gradle, etc.)` from the `Quick Start` options and select Cognitive-Speech-STT-Android folder.

3. When a `Gradle Sync` dialog pops up, choose OK to continue downloading the latest tools.

4. In Android Studio -\> `Project` panel -\> `Android` view, open file "SpeechRecoExample/res/values/strings.xml", and find the line "Please\_add\_the\_subscription\_key\_here;". Replace the "Please\_add\_the\_subscription\_key\_here" value with your subscription key from the first step.

5. If you want to use *Recognition with intent*, you also need to sign up for [Language Understanding Intelligent Service (LUIS)](https://azure.microsoft.com/en-us/services/cognitive-services/language-understanding-intelligent-service/) and set the key values in `luisAppID` and `luisSubscriptionID` in Samples\_SpeechRecoExample\_res\_values\_strings.xml.

6. In Android Studio, select menu `Build` \> `Make Project` to build the sample, and `Run` to launch this sample app.

### Running the sample

In Android Studio, select menu `Run`, and `Run app` to launch this sample app.

1. In the application, press the button `Select Mode` to select what type of speech recognition you would like to use.

2. To start recognition, press the `Start` button.

<img src="SampleScreenshots/SampleRunning1.png" width="50%"/>

## Contributing

We welcome contributions. Feel free to file issues and submit pull requests on the repo and we'll try to address them as soon as possible. Learn more about how you can help on our [Contribution Rules & Guidelines](</CONTRIBUTING.md>).

You can reach out to us anytime with questions and suggestions using our communities below:

* **Support questions:** [StackOverflow](<https://stackoverflow.com/questions/tagged/microsoft-cognitive>)
* **Feedback & feature requests:** [Cognitive Services UserVoice Forum](<https://cognitive.uservoice.com>)

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## License

All Microsoft Cognitive Services SDKs and samples are licensed with the MIT License. For more information, see
[LICENSE](</LICENSE.md>).

Sample images are licensed separately, please refer to [LICENSE-IMAGE](</LICENSE-IMAGE.md>).

## Developer Code of Conduct

Developers using Cognitive Services, including this client library & sample, are expected to follow the "Developer Code of Conduct for Microsoft Cognitive Services", found at [http://go.microsoft.com/fwlink/?LinkId=698895](http://go.microsoft.com/fwlink/?LinkId=698895).
