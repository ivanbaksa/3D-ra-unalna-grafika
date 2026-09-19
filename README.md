# 3D-ra-unalna-grafika
Projekt iz 3D računalne grafike: low-poly animacija



3D Animacija Vožnje Automobila u Low-Poly Stilu (Blender)
Kolegij: 3D Računalna Grafika
Ustanova: Fakultet primijenjene matematike i informatike, Sveučilište Josipa Jurja Strossmayera u Osijeku
Student: Ivan Bakša
Nastavnik / Nositelj kolegija: prof. dr. sc. Domagoj Ševerdija
 
Pregled Projekta
U sklopu ovog projekta izradio sam stiliziranu 3D animaciju kretanja sportskog automobila kroz urbano okruženje u programskom paketu Blender.
Glavni fokus mog rada bio je na primjeni parametarskog modeliranja pomoću krivulja, hijerarhijskoj organizaciji scene pomoću roditeljskih objekata (parenting), automatizaciji gibanja vozila duž staze pomoću ograničenja (constraints) te postavljanju osvjetljenja i dinamične kamere.
 
YouTube Video Animacije
•	Poveznica na video: https://youtu.be/jS9erpWFwqo
 
Korištene Tehnologije i Alati
•	Softver: Blender 3.x / 4.x
•	Render Engine: Eevee (real-time rasterization)
•	Format ispisa: Full HD (1920x1080), 30 FPS, H.264 / MP4
 
Struktura Scene i Tehnike Modeliranja
1.	Automobil (Cube & Cylinder):
o	Karoseriju sam modelirao tehnikom Box Modelinga polazeći od osnovnog primitiva kocke.
o	Koristio sam Mirror Modifier duž uzdužne osi kako bih osigurao savršenu simetriju modela.
o	Kotače sam izradio kao zasebne cilindrične objekte s uvučenim naplatcima pomoću alata Inset i Extrude.
2.	Cesta i rubnjaci (Plane & BézierCurve):
o	Putanju staze i zavoje definirao sam pomoću matematičke Bézier krivulje.
o	Poprečni profil ceste s povišenim rubnjacima proceduralno sam preslikao i savio duž krivulje kombinacijom Array i Curve Modifiera.
3.	Okoliš (Zgrade i Drveće):
o	Zgrade (Cube.001–Cube.008) sam izradio vertikalnim skaliranjem kocki i ekstrudiranjem prozorskih otvora prema unutra.
o	Drveće sam složio modularno kombinacijom suženih valjaka za deblo i niske podjele Icosphere primitiva za krošnje.
o	Na svim elementima okoliša postavio sam ravno sjenčanje (Flat Shading) radi postizanja stiliziranog low-poly izgleda.
 
Sustav Animacije i Hijerarhija
•	Glavni kontroler (Empty): Na vrhu hijerarhije postavio sam pomoćni Empty objekt na koji sam dodao ograničenje Follow Path Constraint.
•	Praćenje krivulje (Follow Curve): Uključivanjem opcije Follow Curve, sustav automatski računa tangente Bézier krivulje i usmjerava vozilo točno u smjeru zavoja bez naglih skokova.
•	Parenting: Karoseriju automobila i kameru podredio sam Empty objektu, čime oni automatski nasljeđuju globalnu translaciju i rotaciju duž staze.
 
Parametri Rendera
•	Ukupan broj frameova: 300 frameova (Start: 1, End: 300)
•	Frame Rate: 30 FPS
•	Trajanje: 10.0 sekundi (300 frameova / 30 FPS)
•	Kamera: Žarišna duljina 50 mm, povišeni 
