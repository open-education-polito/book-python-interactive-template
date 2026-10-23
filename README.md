[![License](https://img.shields.io/github/license/open-education-polito/python-interactive-book-template.svg)](https://github.com/open-education-polito/python-interactive-book-template/blob/master/LICENSE)

# Python Interactive Book Template
> The template files for the Python interactive book

# Status
In sviluppo attivo.

# Indice

- [Come iniziare](#come-iniziare)
- [Come contribuire](#come-contribuire)
- [Manutenzione](#manutenzione)
- [Licenza](#licenza)

# Come iniziare
Questo repo contiene la configurazione per costruire il libro con
[Runestone](https://runestone.academy): `conf.py`, `pavement.py` e le
dipendenze in `requirements.txt`. I contenuti del libro stanno nel repo
[python-interactive-book-chapters](https://github.com/open-education-polito/python-interactive-book-chapters),
che va clonato nella cartella `_sources` (ignorata da git).

## Dipendenze
Python 3.9 o successivo e le librerie in `requirements.txt`
(`runestone>=7.13,<8`).

## Come installare
```bash
git clone https://github.com/open-education-polito/python-interactive-book-template.git libro
cd libro
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
git clone https://github.com/open-education-polito/python-interactive-book-chapters.git _sources
runestone build --all
runestone serve
```
Il libro è in `build/python-interattivo`; `runestone serve` lo pubblica su
`http://localhost:8000`.

## Personalizzazioni rispetto a Runestone
- `_templates/layout.html` è una copia del layout del tema Runestone senza lo
  script pubblicitario EthicalAds. Va riallineata a mano quando si aggiorna
  `runestone`.
- `_static/custom.css` nasconde il messaggio "Log-in to Remove Ads!".
- In `pavement.py`, `minimal_outside_links` toglie i link a login, profilo e
  help di Runestone.
- I ruoli di colore dei capitoli (`:red:`, `:boltblue:`, ...) sono definiti
  in `rst_prolog` in `conf.py`.

## Documentazione
### Link a documentazione esterna
- [Runestone Components](https://github.com/RunestoneInteractive/rs)
- [PreTeXt](https://pretextbook.org): il markup RST di Runestone è deprecato
  e il progetto raccomanda PreTeXt per i libri nuovi.

# Come contribuire
Fai un fork, lavora su un branch e apri una pull request. Prima di aprirla
controlla che `runestone build --all` finisca senza errori.

# Manutenzione 
This project is currently maintained by the `libremente`.


# Licenza 
This repo is covered by a GPL v3.0 license. See `LICENSE` to get more
information about it.

## Licenza generale 

## Autori e Copyright
libremente <surf [AT] libremente [DOT] eu>

## Licenze software dei componenti di terze parti
This is a revision of the original `sphinx-bootstrap` template by the
[Runestone](https://github.com/RunestoneInteractive)
folks. Also their work is covered by a GPL license.
