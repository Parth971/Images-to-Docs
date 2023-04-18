
# Images-to-Docs

Create docs file which contains images from different folders with same filename in tabular form using python.

## Aim

Create a python script which can take images with same from different folder and add in docs file in a structured tablular form.

For example, I have three folders named `abc`, `mvp` and `vcc`. These folders have many images, and some images are of same name in folders. In our case, `N1.png` image is present in all three folders. `N4.png` image is present in `abc` and `mvp` only.

Now, I want a doc file which have one block with name `N1` and under that block there is three images from different folders with corresponding folder names.

## Install Virtual Environment (recommended)

Installing python pakages in virtual environment is recommended.

Install [Python Virtual Environment](https://www.geeksforgeeks.org/creating-python-virtual-environment-windows-linux/)

## Install requirements.txt

After your virtual environment is activated, run below command

    pip install -r requirements.txt

## Run Script

After installing necessary python packages, run below command

    python main.py

### Configs

```
args = (
    ('My 1', r"/home/root366/Dump/GITHUB/Images-to-Docs/abc"),
    ('My 2', r"/home/root366/Dump/GITHUB/Images-to-Docs/vcc"),
    ('My 3', r"/home/root366/Dump/GITHUB/Images-to-Docs/mvp"),
    ...
)
```

In `main.py` file, `args` variable can be changed. Below is description,

`args` is tuple, it contains elements as tuple. Each tuple element in args is having two values. 

In above example, `'My 1'` denotes folder name to be mentioned in docs file. After that, second value is `r"/home/root366/Dump/GITHUB/Images-to-Docs/abc"`. This value denotes, path of folder which contains images. 

- For Linux systems, we can write `r"/home/root366/Dump/GITHUB/Images-to-Docs/abc"`.

- For Windows systems, we can write `r"C:\Users\Parth\Desktop\Currently Working\docs_project\abc"` 

#### Filename

You can change filename of docs generating by changing value of `filename` variable.

Default value is generated from current time

```
filename = f'testing_{current_time.hour}_{current_time.minute}_{current_time.second}.docx'
```
