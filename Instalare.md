# Introducere #

TV-MAXE ar trebui să ruleze pe orice sistem care îndeplineşte cerinţele necesare rulării acestuia. Totuşi instalarea poate fi dificilă pentru utilizatorii care nu folosesc un administrator de pachete, scopul acestui document fiind de a aduna la un loc paşii necesari funcţionării programului TV-MAXE.

# Detalii #

Pentru ca TV-MAXE să funcţioneze aveţi nevoie de următoarele:
  * Python 2.6, cu binding-uri pentru GTK2
  * Clientul oficial de SopCast
  * VLC sau MPlayer (asta în cazul în care nu doriţi utilizarea unui player extern)

**Python** şi **PyGTK** vine preinstalat cu majoritatea distribuţiilor moderne. Dacă distribuţia dumneavoastră nu include aceste programe, le puteţi descărca de pe [site-ul oficial Python](http://www.python.org/) respectiv [site-ul oficial PyGTK](http://www.pygtk.org/).

Versiunea binară a clientului oficial de **SopCast** (sp-sc-auth) poate fi descărcat [de aici](http://download.easetuner.com/download/sp-auth.tgz). Din păcate se pare că nu există o variantă open-source a acestui program. Ţineţi cont că, pentru a rula _sp-sc-auth_ aveţi nevoie de **libstdcpp5**. O versiune precompilată pentru platforma x86-32 poate fi descărcată [de aici](http://www.sopcast.com/download/libstdcpp5.tgz). Utilizatorilor Ubuntu li se recomandă activarea depozitelor _universe_ (în Ubuntu 10.10) sau _backports_ (în Ubuntu 10.04) şi actualizarea listei de pachete înainte de instalarea TV-MAXE. Pentru mai multe detalii vizitaţi [documentaţia](https://help.ubuntu.com/community/Repositories/Ubuntu).

**VLC**, respectiv **MPlayer**, se regăsesc şi ele în depozitele marilor distribuţii. Pentru TV-MAXE se recomandă utilizarea backend-ului VLC, însă programul funcţionează fără probleme şi cu MPlayer. Utilizatorii de Ubuntu 10.04 sau mai vechi vor trebui să îşi actualizeze versiunea de VLC la cel puţin 1.1.0. Citiţi cu atenţie licenţele programelor MPlayer şi VLC! Utilizarea acestora poate fi ilegală în anumite state.