import random
import numpy as np
import pandas as pd
from sklearn.datasets import make_regression
from sklearn.model_selection import train_test_split

pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('data creation') {
      steps {
        sh 'python3 data_creation.py'
        echo 'Done'
      }
    }
  }
}
