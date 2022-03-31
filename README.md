
<!-- Find and Replace All [repo_name] -->
<!-- Replace [product-screenshot] [product-url] -->
<!-- Other Badgets https://naereen.github.io/badges/ -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
<!-- [![License][license-shield]][license-url] -->


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <!-- <a href="#overview-of-the-analysis">Overview of the Analysis</a> -->
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#evaluation-report">Evaluation Report</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
	<!-- <li><a href="#license">License</a></li> -->
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This is an Application that implements an algorithmic trading strategy that uses machine learning to automate the trade decisions.

#
#### *** Disclaimer! This application is for educational purposes only and not intended for financial advice.  The dataset used is historical OHLC price data from an emerging market asset.  The symbol of the asset is not disclosed due to this app being developed strictly for educational purposes only ***
#

### Built With

<!-- This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples. -->

* [Python](https://www.python.org/)
* [Python conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)
* [Python JupyterLab](https://jupyter.org/)
* [Python CSV Reading/Writing](https://docs.python.org/3/library/csv.html)
* [Python pandas](https://pandas.pydata.org/)
* [Python scikit-learn](https://scikit-learn.org/stable/)

## Evaluation Report

#### Overview of the Analysis

* The purpose of the analysis is to train a model that uses machine learning to automate the trade decisions.
* The dataset is historical OHLC price data from an emerging market asset.  The symbol of the asset is not disclosed due to this app being developed for educational purposes.
* The variables that is being predicted is the `signals_df['Signal']` column which is calculated based on the cross of two moving averages used as a trigger.  The moving averages are assigned to the `X` variable : `X = signals_df[['SMA_Fast', 'SMA_Slow']]` and the `y` variable is assigned the value of : `signals_df['Signal']` for the model.
* Rules :
  - When the `SMA_Slow` crosses the `SMA_Fast` from a lower to a higher price it sends a `1` to the `y` `(signal)` variable
  - Wen the `SMA_Slow` crosses the `SMA_Fast` from a higher to a lower price it sends a `-1` to the `y` `(signal)` variable
  - A `1`=`Buy` and `-1`=`Sell`.
* Assumption - FULL DISCLOSURE - This model assumes that the trader is able to consistently enter the market at the previous day close.  This is a critical and dangerous assumption since it assumes 100% accuracy and 100% success in the price of the market entry for the `Actual Returns` calculation.  A more realistic and accurate entry strategy will be needed in order to fine tune a profit strategy, but this was beyond the scope of this analysis. Understanding the risk and assumption of the model proves this to be a good model since the machine learning aspect of the analysis was proven and it was profitable.
* I build 3 models.  First I established a `Baseline Performance`, then build a model based on `Support Vector Machine` method and then a `LogisticRegression` model.

#### Summary of Analysis

* The `Baseline Strategy` performance was very good overall considering the response during periods on volatility in the market.  The  `Strategy Returns` column yielded better results thant the `Actual Returns` column for this strategy almost consistently
[Baseline Screenshot][baseline-screenshot]


<!-- GETTING STARTED -->
## Getting Started

<!-- This is an example of how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple example steps. -->
* Install and import the required libraries and dependencies ONLY as needed!

* You don't need Python installed in your computer. You can install Anaconda and JupyterLab normally just like any other application on your computer. Follow the instructions for Anaconda, ensure that its working, then install JupyterLab.

* I have placed Comments throughout the code so that you can follow the code and be able to replicate the app on your own. Also, so that you're able to contribute in the future :-)

### Prerequisites

<!-- This is an example of how to list things you need to use the software and how to install them. -->
A text editor such as [VS Code](https://code.visualstudio.com/) or [Sublime Text](https://www.sublimetext.com/)


### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/AnaIitico/machine_learning_trading_bot.git
   ```

2. You don't need to install pip - Conda comes with pip and you can also use the command
    conda install 'package name'
   
3. Install Conda according to the instructions based on your operating system.
    For windows users you MUST use the Administrator PowerShell. Users with AMD Processors MUST use the Administrator PowerShell 7 (X64) version
  
    Once installed Conda has an Admin PowerShell version shortcut - look on your Start menu for it.
    This shortcut will prove very useful at times when you need to install other apps or make adjustments to your installation

    Once installed you will see (base) on your terminal
   
4. Activate Conda Dev environment
   ```sh
   conda activate dev
   ```
   You should now see (dev) on your terminal

5. Install JupyterLabs
   ```sh
   pip install jupyterlab
   ```

6. Run JupyterLabs
   ```sh
   jupyter lab
   ```
   A browser window should open on localhost:8888/lab

<!-- USAGE EXAMPLES -->
## Usage
  
<!-- Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources. -->

<!-- ROADMAP -->

## Roadmap

  The app is finished
<!-- Here are some screenshots and code snippets of the working app

#### Exchange Comparison January 2018
![Exchange January Screen Shot][exchange-january-screenshot]

#### Exchange Comparison March 2018 - With Analysis
![Exchange March Screen Shot][exchange-march-screenshot]


#### Calculate Arbitrage Profits Snippet - for January 16 only
#### you can see the full code (with outputs) in the [machine_learning_trading_bot.ipynb](https://github.com/AnaIitico/machine_learning_trading_bot/blob/main/machine_learning_trading_bot.ipynb) file
  *This code has been summarized into one block for convenience*
  *and there's an analysis at the end*
```sh
  # some cool code here
 ``` -->

See the [open issues](https://github.com/AnaIitico/machine_learning_trading_bot/issues) for a list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->
<!-- ## License

Distributed under the MIT License. See `LICENSE` for more information.
 -->

<!-- CONTACT -->
## Contact

Jose Tollinchi - [@josetollinchi][linkedin-url] - jtollinchi1971@gmail.com

Project Link: [https://github.com/AnaIitico/machine_learning_trading_bot](https://github.com/AnaIitico/machine_learning_trading_bot)

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

Other Dependencies used to build the project.
##### Search google for the correct conda install command

* numpy
* hvplot
* matplotlib

* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/AnaIitico/machine_learning_trading_bot.svg?style=for-the-badge
[contributors-url]: https://github.com/AnaIitico/machine_learning_trading_bot/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/AnaIitico/machine_learning_trading_bot.svg?style=for-the-badge
[forks-url]: https://github.com/AnaIitico/machine_learning_trading_bot/network/members
[stars-shield]: https://img.shields.io/github/stars/AnaIitico/machine_learning_trading_bot.svg?style=for-the-badge
[stars-url]: https://github.com/AnaIitico/machine_learning_trading_bot/stargazers
[issues-shield]: https://img.shields.io/github/issues/AnaIitico/machine_learning_trading_bot/network/members?style=for-the-badge
[issues-url]: https://github.com/AnaIitico/machine_learning_trading_bot/issues
<!-- [license-shield]: 
[license-url]:  -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/josetollinchi/
<!-- [exchange-january-screenshot]: /images/exchange_january_2018.JPG
[exchange-march-screenshot]: /images/exchange_march_2018.JPG -->
[baseline-screenshot]: images/baseline_strategy_returns.png