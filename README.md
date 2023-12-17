# Doporučovací systémy

Tento projekt je určen jako učební materiál pro podporu výuky umělé inteligence na 
[Smíchovské střední průmyslové škole a gymnáziu](https://ssps.cz).

V této ukázce si zkusíme implementovat jednoduchý doporučovací systém filmů na základě dříve vyplněných
hodnocení (viz [zde](https://vojtechpavlu.github.io/movies-frontend/)).

Pro zajištění stejného prostředí, jaké jsem měl já, proveďte následující kroky:

1. [Ověření Pythonu](#ověření-pythonu)
2. [Ověření balíčkovacího manažeru](#ověření-balíčkovacího-manažeru)
3. [Instalace virtuálního prostředí](#instalace-virtuálního-prostředí) *(volitelné)*
4. [Instalace a spuštění prostředí Jupyter Notebook](#instalace-a-spuštění-prostředí-jupyter-notebook)
5. [Vytvoření datového adresáře](#vytvoření-datového-adresáře) *(volitelné)*


## Před spuštěním

Pro spuštění je předpokládán nainstalovaný [Jupyter Notebook](https://jupyter.org/) coby běhové 
prostředí. 

Alternativně však lze použít i další vývojová prostředí:
- [PyCharm](https://www.jetbrains.com/pycharm/)
- [JupyterLab](https://jupyter.org/)
- [Google Colab](https://colab.google/)
- [VS Code s příslušnými rozšířeními](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)
- [Apache Zeppelin](https://zeppelin.apache.org/)

Já osobně práci s notebooky preferuji právě lokální Jupyter; rozhodnete-li se jinak, můžete 
následující kroky směle přeskočit 😉


### Ověření Pythonu

Prvním krokem je však pochopitelně ověření, že máte nainstalován a správně nastaven Python:

```shell
python --version
```

V některých operačních systémech je Python ukryt pod jinými klíčovými slovy:

```shell
py --version
```

či případně

```shell
python3 --version
```

V takovém případě si klíčové slovíčko `python` nahraďte vyhovujícím.


### Ověření balíčkovacího manažeru

Dále ověřte, že máte nainstalován pythoní balíčkovací manažer:


```shell
python -m pip --version
```

Pokud tento nemáte nainstalován, pokračujte [zde](https://pip.pypa.io/en/stable/installation/).


### Instalace virtuálního prostředí

Virtuální prostředí je doporučená praktika pro instalace balíčků na Vaše zařízení. Dokážete tak 
oddělit jednotlivé projekty, které mohou využívat různé verze Vámi instalovaných knihoven.

Jde o nepovinný krok, ale doporučený; minimálně kvůli tomu, že budete mít větší kontrolu nad tím,
co skutečně instalujete. Uvážíte-li tedy za vhodné, můžete tento krok přeskočit na 
[další krok](#instalace-prostředí-jupyter-notebook).


Na Windows nainstalujete virtuální prostředí (dále jen *venv*) pomocí následujících příkazů.

V prvním kroku musíte virtuální prostředí získat (nainstalovat):

```shell
python -m pip install venv
```

Následně ho inicializujete:

```shell
python -m venv [vámi_vybraná_složka]
```

(osobně preferuji zajít do cílové složky, pak použiji `python -m venv .`)

Posledním krokem je jeho spuštění (Windows):

```shell
[vámi_vybraná_složka]\bin\Activate.bat
```

Pro Unixová prostředí:

```shell
source [vámi_vybraná_složka]/bin/Activate.bat
```

Pro více informací o virtuálním prostředí se podívejte 
[zde](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/).


### Instalace a spuštění prostředí Jupyter Notebook

Nyní stačí nainstalovat a spustit Jupyter pomocí následujících příkazů:

```shell
pip install jupyter
```

Spustíte ho pomocí:

```shell
jupyter notebook
```

Tento příkaz by Vám měl otevřít defaultní prohlížeč s reprezentací aktuální vybrané složky.


### Vytvoření datového adresáře

Abyste měli přístup k datům, se kterými jsem pracoval, a abyste si mohli nasimulovat celé workflow, 
vytvořte si adresář `[vámi_vybraná_složka]/data`, do kterého vložíte všechny tři datové soubory, které jsem Vám již dříve
nasdílel:

- `movies.json`
- `users.json`
- `ratings.json`


### Ukončení virtuálního prostředí

Pro ukončení virtuálního prostředí (použili-li jste ho) stačí zadat následující příkaz v konzoli:

```shell
deactivate
```

🎉 ***Happy Coding!*** 🎉
