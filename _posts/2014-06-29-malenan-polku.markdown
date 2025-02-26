---
layout: post
title: "MALENAN POLKU"
start_date: Kampissa 29.06.2014
end_date: 29.06.2016
categories: jekyll update
---

###### Historiaa Kampissa. Äänikuvia ja kuvakertomus erään kamppilaisen kokemuksesta alati muuttuvassa ympäristössä.

## REITTI

![image](/images/kartta1.png)

**1** Vanha linja-autoasema / **2** Mercatorkuja, Mannerheimintie 20, Yrjönkatu / **3** Simonkatu 10, Yrjönkatu 38 (jugendtalo Pietola) / **4** Tavastia Club, Urho Kekkosen katu 4-6 / **5** Lapinrinne 2, talo / **6** Ravintola Torni, Yrjönkatu 26 / **7** Vanha kirkkopuisto, Ruttopuisto / **8** Eerikinkatu kokonaan / **9** Hietalahdentie 3 / **10** Hietalahdentori

## ÄÄNI JA KUVAT 

#### **1.** Vanha linja-autoasema

<button class="play-button" data-audio="/audio/kamppi/01.mp3">▶</button>

![image](/images/01.jpg)

#### **2.** Mercatonkuja, Mannerheimintie 20, Yrjönkatu

<button class="play-button" data-audio="/audio/kamppi/02.mp3">▶</button>

![image](/images/02.jpg)

#### **3.** Simonkatu 10, Yrjönkatu 38 (jugendtalo Pietola)

<button class="play-button" data-audio="/audio/kamppi/03.mp3">▶</button>

![image](/images/03.jpg)

#### **4.** Tavastia Club, Urho Kekkosen katu 4-6

<button class="play-button" data-audio="/audio/kamppi/04.mp3">▶</button>

![image](/images/04.jpg)

#### **5.** Lapinrinne 2, talo

<button class="play-button" data-audio="/audio/kamppi/05.mp3">▶</button>

![image](/images/05.jpg)

#### **6.** Ravintola Torni, Yrjönkatu 26

<button class="play-button" data-audio="/audio/kamppi/06.mp3">▶</button>

![image](/images/06.jpg)

#### **7.** Vanha kirkkopuisto, Ruttopuisto

<button class="play-button" data-audio="/audio/kamppi/07.mp3">▶</button>

![image](/images/07.jpg)

#### **8.** Eerikinkatu kokonaan

<button class="play-button" data-audio="/audio/kamppi/08.mp3">▶</button>

![image](/images/08.jpg)

#### **9.** Hietalahdentie 3

<button class="play-button" data-audio="/audio/kamppi/09.mp3">▶</button>

![image](/images/09.jpg)

#### **10.** Hietalahdentori

<button class="play-button" data-audio="/audio/kamppi/10.mp3">▶</button>

![image](/images/10.jpg)

**Konsepti:** Maj-Britt Huovila **Kuvat:** Johannes Romppanen, Emil Romppanen, Risto Törrö **Audio:** Jyri Pirinen **Teksti:** Laura Hyyti 

<script>
    document.addEventListener("DOMContentLoaded", function () {
        document.querySelectorAll(".play-button").forEach(button => {
            button.addEventListener("click", function () {
                const audioSrc = this.getAttribute("data-audio");
                let audio = document.getElementById("audio");

                if (!audio) {
                    audio = document.createElement("audio");
                    audio.id = "audio";
                    document.body.appendChild(audio);
                }

                // If the same button is clicked again, toggle play/pause
                if (audio.src !== window.location.origin + audioSrc) {
                    audio.src = audioSrc;
                    audio.play();
                    resetButtons();
                    this.textContent = "■"; // Change button to pause icon
                } else {
                    if (audio.paused) {
                        audio.play();
                        this.textContent = "■";
                    } else {
                        audio.pause();
                        this.textContent = "▶";
                    }
                }

                // Pause all other audio buttons
                function resetButtons() {
                    document.querySelectorAll(".play-button").forEach(btn => {
                        if (btn !== button) {
                            btn.textContent = "▶"; // Reset other buttons
                        }
                    });
                }
            });
        });
    });
</script>
