# universetech-lotterydraw

<h3><a href="http://35.234.20.231:8000/demo/">LIVE DEMO</a></h3>

A backend implement with lottery draw as topic based on calling other web API.

<p float="left">
  <img src="https://github.com/j3ygithub/universetech-lotterydraw/blob/master/docs/images/sc1.jpg" width="50%">
</p>

## Installation

This requires python 3.7.7 or higher.

First, cd to your repos dir and do the following commands to install all the python packages:

OS X & Linux:

```
git clone https://github.com/j3ygithub/universetech-lotterydraw
cd universetech-lotterydraw
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Windows:

```
git clone https://github.com/j3ygithub/universetech-lotterydraw
cd universetech-lotterydraw
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

Then you can use <a href='https://github.com/pyinvoke/invoke'>invoke</a> to do the following operations:

initialize DB
```
invoke migrate
```

create some fake data in DB for testing
```
invoke createdata
```

delete all the data (you can create them again though)
```
invoke deletedata
```

And to update the data you will need to run the servers:

```
python onefake/manage.py runserver 8001 &
python twofake/manage.py runserver 8002 &
python twofake/manage.py runserver 8000
```
> You may need to run it on different cmd if you're on a windows OS. 

Then you could browse
```
http://127.0.0.1:8000/demo
```

and you can test its create, update, delete features or use invoke commands on terminal like:
```
invoke updatedata
```

For more details, please check https://github.com/j3ygithub/universetech-lotterydraw.


## Meta

Jimmy Lin <b00502013@gmail.com>

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/j3ygithub/](https://github.com/j3ygithub/)

## Contributing

1. Fork it (<https://github.com/j3ygithub/universetech-lotterydraw/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request
