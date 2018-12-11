#### Uporaba zunanjega API-ja za generiranje slik v tekst:
http://textart.io/api/img2txt
```mermaid
graph LR;
A[UserService];
B[PhotoSerivce];
C[AlbumSerivce];
D[CommentService];
E[ShareService];
F[ImageToTextService];
A-->|pridobi slike uporabnika|B;
A-->|pridobi albume uporabnika|C;
A-->|pridobi komentarje uporabnika|D;
B-->|pridobi slike albuma|C;
B-->|pridobi komentarje slike|D;
A-->|pridobi kolaže uporabnika|F;
A-->|pridobi deljene slike|E;
E-->|pridobi slike|B;
A-->|pridobi deljene albume|C;
E-->|pridobi albume|C;
F-->|pridobi slike|B;
F-->|pridobi lastnika slike|A
A-->|pridobi textovne slike za uporabnika|F

Github zaenkat še ne podpira mermaid markupa tako da je spodej slika.

```
![Klici med mikrostoritvami](mermaid-diagram-20181211150816.svg)