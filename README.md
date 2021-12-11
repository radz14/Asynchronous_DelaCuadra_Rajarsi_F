# Asynchronous_DelaCuadra_Rajarsi_F
Asynchronous
# install Pint if necessary

try:
    import pint
except ImportError:
    !pip install pint
    from os.path import basename, exists

def download(url):
    filename = basename(url)
    if not exists(filename):
        from urllib.request import urlretrieve
        local, _ = urlretrieve(url, filename)
        print('Downloaded ' + local)
    
download('https://raw.githubusercontent.com/AllenDowney/' +
         'ModSimPy/master/modsim.py')
