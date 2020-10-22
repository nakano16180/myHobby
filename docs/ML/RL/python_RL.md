### 環境構築

#### Python Setup
```
$ sudo apt install virtualenv
```

#### ソースコード
```
$ git clone https://github.com/icoxfog417/baby-steps-of-rl-ja.git
$ cd baby-steps-of-rl-ja/

$ virtualenv -p python3.6 venv
$ source venv/bin/activate

$ pip3 install -r requirements.txt
$ pip3 uninstall tensorflow
$ pip3 install tensorflow-gpu==1.14.0

```

bashrcに以下を追記

```
$ export TF_FORCE_GPU_ALLOW_GROWTH=true
```