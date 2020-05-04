+++
author = "Marco Cornaggia"
title = "Usare la funzione stop-limit su Binance"
date = "2020-04-25"
description = "Benvenuto! In questo breve articolo vediamo come impostare lo stop-loss su Binance e andare a letto così tranquilli"
tags = [
    "bitcoin",
]
+++

In questo breve articolo vediamo come realizzare un comodo password manager con Python. 
<!--more-->
Tutto ciò che ci occorre è l'ultima versione di [`Python`](https://www.python.org/downloads/) sul nostro pc e la libreria [Piperclip](https://pypi.org/project/pyperclip/). 

Una volta fatto ciò, possiamo creare un nuovo documento e rinominarlo "Password Manager".


<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

Di seguito potete copiare il codice che ho realizzato, salvare il vostro programma su Desktop e cliccare sul tasto "Run".

***

**N.B.** L'esempio di seguito è stato realizzando usando un dizionario di password. A ciascuna password corrisponde un sito.

{{< highlight html >}}
import pyperclip

psw = {
    'sito1':'password1',
    'sito2':'password2',
	'sito3':'password3',
	'sito4':'password4',
	'sito5':'password5',
    'sito6':'password6'
    }

print("\nCiao Marco! Di quale password hai bisogno?") #inserisci il tuo nome
for sito in psw:
    print(" -"+sito)

sito_scelto = input()
password_scelta = psw[sito_scelto]
pyperclip.copy(password_scelta)

print("\nCopiata! Ora non ti resta che incollarla")
input()

{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji,Segoe UI Emoji,NotoColorEmoji,Segoe UI Symbol,Android Emoji,EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
    .nowrap {
	display: block;
	margin: 25px 0;
}
}
</style>
{{< /css.inline >}}