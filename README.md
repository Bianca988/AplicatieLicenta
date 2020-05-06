# AplicatieLicenta
Trebuie sa afisez harta indoor a unui spatiu creat pe site-ul indooratlas , care ofera sdk-ul propriu ,api key-uri
Am considerat ca afisarea harti este similara cu cea a unei harti outdoor(exemplu google maps gasit pe internet)
In final am gasit exemplu pe site-ul celor de la indooratlas , dar am o problema cu partea de fragmenetactivity
care ma ajuta sa afisez.
Am cautat eroarea : android.view.InflateException: Binary XML file line #9: Binary XML file line #9: Class is not a View com.example.probaharta.MainActivity
Au intampinat-o din ce am observat mai multi oameni(norocul meu ) : 
Acesta e cel mai bun raspuns pe care l-am gasit : 
It happens because the activity that starts fragment doesn't use a Material or AppCompat theme.
It's not your activity, it comes from the testing library.
You can instruct which theme to use by calling :
launchInContainer(Class fragmentClass, Bundle fragmentArgs, int themeResId, FragmentFactory factory) " 


in loc de launchincontainer cred ca ar fi denumirea clasei mele dar nu am reusit sa implementez . 


Api urile folosite pentru harta le-am introdus in fisieul manifest pentru indooratlas iar cele pentru google in
fisierul google_maps_api.xml - pentru ca aplicatia doresc sa localizele spaptiul prin intermediul google maps si 
site.

Aplicatia fiind inspirata si de pe site-ul lor cred ca e scrisa corect mai putin partea de fragment care da eroare

Aplicatia nu se poate porni din virtual device .
Contine un mainActivity2 care are un buton spre deschiderea hartii
care ar fi clasele :MainActivity care depinde de bluedot si bluedotmove estimate create pentru localizare in timp 
ce utilizatorul se misca 


Multumesc! 
