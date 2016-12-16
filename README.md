# DataSets 
* Contains 10 datasets to be used as training and testing data sets, generated using 'generateSimulatedDataSets.R'
* these datasets are used in 'turbineClassification.R' code

# WorkSpaceData
* initWrkSpc.RData : has an image of the workspace with all the functions sourced. No need to source individual functions separately unless they are changed.
* nnetFSv2.RData : has the model obtained after feature selection with NNET

# Results
* Contains various ROC values for various classifiers with various pre-processing options

# WorkingCodes
* cartesian2LatLon.R and latLon2Cartesian.R : converts from latitude-longitude to cartesian coordinates and vice-versa
* classifyTurbines.R : classification code for training various classifier models to predict probability of turbine damage
* demoCode.R : demo code presenting most of the functionalities created
* estimateBivariateGaussianParams.R : estimates the parameters of the bivariate gaussian distribution for each lightning strike ellipse
* generateClassifierAttributes.R : generates the proposed attributes for each turbine based on the lightning data set
* generateSimulatedDataSets.R : generates simulated training and testing data sets to be used for classification
* getClassPrediction.R : takes a list of classifier models and turbine data set and returns the predictions for each turbine
* getEllipseData.R : returns points in 2D for plotting ellipse
* getEnsembleClassifier.R : takes a list of trained classifier models and returns an ensemble classifier combining the predictions generated by the trained classifier models using stack generalization method
* getEnsembleClassifierAttributes.R : generates data set for ensemble classification
* getOptimalFeature.R : finds optimal subset of proposed attributes to improve classifier performance
* initSetup.R : installs and load required packages and a workspace image
* isPointInEllipse.R : checks if a point is inside an ellipse
* lightStrikeOracle.R : takes a training set based on a past storm and turbine locations, trains a list of classifier models and predicts turbine damage for another storm
* lightStrikeSimulator.R : simulates lightning strikes based on the new lightning data set provided, done by Undergrad team, modified to fit other codes
* OptimalFeaturesMain.R : main code for performing feature selection
* plotTurbineStrikeCount.R : plots turbine strike count attribute for visual representation
* plotProbabilityContours.R : plots contours for strike location probability
* plotROCs.R : plots ROC curves for a list of models
* plotTurbineAttributes.R : plots proposed turbine attributes
* plotTurbineDamageProbability.R : plots rank ordered list of turbine damage based on predicted probability
* plotTurbineLightStrikeOverlapArea.R : visual representation plot for computing overlap area between light strike ellipse and attractive region of turbine
* predictorAttributeROC.R : computes the ROC values for a list of attribute values
* preProcessLightningData.R : pre-processes lightning data read from excel sheet provided by GE, to format the data in a form usable by the rest of the codes
* preProcessTurbineData.R : pre-processes Turbine data provided by GE
* readData.R : reads the excel sheets provided by GE
* simulateTurbineDamage.R : simulates ground truth data (turbine damage)
* turbineClassification.R : code for performing classification for different sets of training and testing data sets and produce 'AUROC' values
* turbineStrikeOverLapAreaAttributes.R : generates attributes related to area of overlap between light strike ellipses and attractive region of turbines
* turbineStrikeProbabilityAttributes.R : generates attributes related to strike location probability defined by the bivariate gaussian distribution
* updateClassifier.R : updates pre-existing trained classifier models as new grounf truth data becomes available (this needs more work, and I'll continue working on it)
* visualizeLightningData.R : visualization of lightning data set
* plotTurbineDamageProbability.R : plots rank-ordered list of turbines being damaged

* Main file to look at will be lightStrikeOracle.R which is used for all the computation for the UI backend.
   demoCode.R runs a demo of lightStrikeOracle.R *> Do run this to see what results are produced.
   Most of the codes here are functions. So do not forget to source them if you make changes.
   Also most of the codes implement 'parallelization' *> so be a bit careful how you use those codes.


# Contact
Please contact through email 'sahas3@rpi.edu' in case of any queries or to report any bugs. Thanks !

# 
As I'll work on some aspects of the codes, I'll host the new versions of the codes at tinyurl.com/sahaCourses in case anyone is interested in those updates.
