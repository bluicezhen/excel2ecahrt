# excel2echart

A python tool for transform excel file to eChart HTML.

## 1. Installation

```bash
git clone git@github.com:bluicezhen/excel2ecahrt.git
cd excel2echart
pipenv install
mkdir bin
cat > ./bin/excel2ecahrt.sh <<- EOF
#!/bin/bash
filename="\$1"
$(pipenv --venv)/bin/python $(pwd)/excel2echart.py "\$filename"
EOF
chmod +x ./bin/excel2ecahrt.sh
echo "export PATH="$(pwd)/bin:$PATH" >> ~/.bash_profile
```

## 2. Use

```bash
excel2ecahrt.sh some.xlsx
```

## 3. Excel example

| date       | bbl   | bmt   | gy    | xq   | ldjj  | mn    | sllh  | wd    |
| ---------- | ----- | ----- | ----- | ---- | ----- | ----- | ----- | ----- |
| 2022-05-26 |       | 100.5 | 118.2 |      | 109.3 | 76.3  |       | 57    |
| 2022-05-30 |       | 108.5 |       |      |       |       |       |       |
| 2022-06-06 |       | 166.8 | 153.7 | 83.1 | 145.7 | 131.6 | 86.6  | 119.1 |
| 2022-06-13 |       |       | 162.3 |      |       |       |       |       |
| 2022-06-14 |       |       |       |      |       |       | 88.7  |       |
| 2022-06-15 |       |       |       |      |       |       | 90.5  |       |
| 2022-06-16 |       |       |       |      |       |       | 115.9 |       |
| 2022-06-19 |       |       |       |      |       |       | 117.1 |       |
| 2022-06-21 | 142.3 |       |       |      |       |       | 117.7 |       |
| 2022-06-22 | 146.4 |       |       |      |       |       | 117.7 |       |