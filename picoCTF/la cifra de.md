## Descripcion

I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 58295`. 

## Pistas

There are tools that make this easy.


## Solución

``` 
Accedemos a a webshell y nos da el siguiente texto:
Ne iy nytkwpsznyg nth it mtsztcy vjzprj zfzjy rkhpibj nrkitt ltc tnnygy ysee itd tte cxjltk

Ifrosr tnj noawde uk siyyzre, yse Bnretèwp Cousex mls hjpn xjtnbjytki xatd eisjd

Iz bls lfwskqj azycihzeej yz Brftsk ip Volpnèxj ls oy hay tcimnyarqj dkxnrogpd os 1553 my Mnzvgs Mazytszf Merqlsu ny hox moup Wa inqrg ipl. Ynr. Gotgat Gltzndtg Gplrfdo 

Ltc tnj tmvqpmkseaznzn uk ehox nivmpr g ylbrj ts ltcmki my yqtdosr tnj wocjc hgqq ol fy oxitngwj arusahje fuw ln guaaxjytrd catizm tzxbkw zf vqlckx hizm ceyupcz yz tnj fpvjc hgqqpohzCZK{m311a50_0x_a1rn3x3_h1ah3xf966878l}

Tnj qixxe wkqw-duhfmkseej ipsiwtpznzn uk l puqjarusahjeii htpnjc hubpvkw, hay rldk fcoaso 1467 be Qpot Gltzndtg Fwbkwei.

Zmp Volpnèxj Nivmpr ox ehkwpfuwp surptorps ifwlki ehk Fwbkwei Jndc uw Llhjcto Htpnjc.

It 1508, Ozhgsyey Ycizmpmozd itapnzjo tnj do-ifwlki eahzwa xjntg (f xazwtx uk dhokeej fwpnfmezx) ehgy hoaqo lgypr hj l cxneiifw curaotjyt uk ehk Atgksèce Inahkw.

Merqlsu’x deityd htzkrje avupaxjo it 1555 fd a itytosfaznzn uk ehk ktryy. Ehk qzwkw saraps uk ehk fwpnfmezx lrk szw ymtfzjo rklflgwwy, hze tnj llvmlbkyd ati ehk nydkc wezypry fce sniej gj mkfys uk l mtjxotnn kkd ahxfde, cmtcn hln hj oilkprkse woys eghs cuwceyuznjjyt

accedemos a https://gchq.github.io/CyberChef/#recipe=Vigenère_Decode('flag')&input=TmUgaXkgbnl0a3dwc3pueWcgbnRoIGl0IG10c3p0Y3kgdmp6cHJqIHpmemp5IHJraHBpYmogbnJraXR0IGx0YyB0bm55Z3kgeXNlZSBpdGQgdHRlIGN4amx0aw0KDQpJZnJvc3IgdG5qIG5vYXdkZSB1ayBzaXl5enJlLCB5c2UgQm5yZXTDqHdwIENvdXNleCBtbHMgaGpwbiB4anRuYmp5dGtpIHhhdGQgZWlzamQNCg0KSXogYmxzIGxmd3NrcWogYXp5Y2loemVlaiB5eiBCcmZ0c2sgaXAgVm9scG7DqHhqIGxzIG95IGhheSB0Y2ltbnlhcnFqIGRreG5yb2dwZCBvcyAxNTUzIG15IE1uenZncyBNYXp5dHN6ZiBNZXJxbHN1IG55IGhveCBtb3VwIFdhIGlucXJnIGlwbC4gWW5yLiBHb3RnYXQgR2x0em5kdGcgR3BscmZkbyANCg0KTHRjIHRuaiB0bXZxcG1rc2Vhem56biB1ayBlaG94IG5pdm1wciBnIHlsYnJqIHRzIGx0Y21raSBteSB5cXRkb3NyIHRuaiB3b2NqYyBoZ3FxIG9sIGZ5IG94aXRuZ3dqIGFydXNhaGplIGZ1dyBsbiBndWFheGp5dHJkIGNhdGl6bSB0enhia3cgemYgdnFsY2t4IGhpem0gY2V5dXBjeiB5eiB0bmogZnB2amMgaGdxcXBvaHpDWkt7bTMxMWE1MF8weF9hMXJuM3gzX2gxYWgzeGY5NjY4NzhsfQ0KDQpUbmogcWl4eGUgd2txdy1kdWhmbWtzZWVqIGlwc2l3dHB6bnpuIHVrIGwgcHVxamFydXNhaGplaWkgaHRwbmpjIGh1YnB2a3csIGhheSBybGRrIGZjb2FzbyAxNDY3IGJlIFFwb3QgR2x0em5kdGcgRndia3dlaS4NCg0KWm1wIFZvbHBuw6h4aiBOaXZtcHIgb3ggZWhrd3BmdXdwIHN1cnB0b3JwcyBpZndsa2kgZWhrIEZ3Ymt3ZWkgSm5kYyB1dyBMbGhqY3RvIEh0cG5qYy4NCg0KSXQgMTUwOCwgT3poZ3N5ZXkgWWNpem1wbW96ZCBpdGFwbnpqbyB0bmogZG8taWZ3bGtpIGVhaHp3YSB4am50ZyAoZiB4YXp3dHggdWsgZGhva2VlaiBmd3BuZm1lengpIGVoZ3kgaG9hcW8gbGd5cHIgaGogbCBjeG5laWlmdyBjdXJhb3RqeXQgdWsgZWhrIEF0Z2tzw6hjZSBJbmFoa3cuDQoNCk1lcnFsc3XigJl4IGRlaXR5ZCBodHprcmplIGF2dXBheGpvIGl0IDE1NTUgZmQgYSBpdHl0b3NmYXpuem4gdWsgZWhrIGt0cnl5LiBFaGsgcXp3a3cgc2FyYXBzIHVrIGVoayBmd3BuZm1lenggbHJrIHN6dyB5bXRmempvIHJrbGZsZ3d3eSwgaHplIHRuaiBsbHZtbGJreWQgYXRpIGVoayBueWRrYyB3ZXp5cHJ5IGZjZSBzbmllaiBnaiBta2Z5cyB1ayBsIG10anhvdG5uIGtrZCBhaHhmZGUsIGNtdGNuIGhsbiBoaiBvaWxrcHJrc2Ugd295cyBlZ2hzIGN1d2NleXV6bmpqeXQK
 y ponemo flag.

```

## Bandera
Flag: picoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a}




## Notas adicionales


## Referencias
