> [!NOTE]
>  THIS IS NOT WHAT YOU'RE LOOKING, THIS IS JUST TURKISH VERSION, YOU CAN GO TO THE MAIN GUIDE [HERE](https://github.com/yokoffing/NextDNS-Config)

***
# Kılavuz ilkeler :bookmark:
1) [Azalan getiriler yasasını]() kullanarak aşırı engellemeyi önleyin (örneğin, [aklı başında](https://www.privacyguides.org/en/basics/threat-modeling/), kaliteli [blok listeleri](https://github.com/yokoffing/NextDNS-Config#blocklists-1) kullanmak; çoğu [TLD'ye](https://github.com/yokoffing/NextDNS-Config#block-top-level-domains-tlds-1-2-3-4-5-);izin vermek vesaire.).
2) Birkaç istisna dışında [kız arkadaş testini](https://www.urbandictionary.com/define.php?term=Grandma%20Test) geçin. Bu sapmalar kılavuz boyunca belgelenmiştir.

***

## Hesabınızı oluşturun

NextDNS için kayıt olun [buradan](https://nextdns.io/?from=xujj63g5) ve yokoffing'nin hazırladığı kılavuza destek olun!

***

# Güvenlik :police_officer:

Güvenlik ayarları verilerinizi zarara, hırsızlığa ve yetkisiz kullanıma karşı korur.<sup>*^[Neden bu önemli?](https://thenewoil.org/en/guides/prologue/why)*</sup>

## Tehdit İstihbaratı Beslemeleri <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/threat-intelligence-feeds.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Tehdit istihbaratı beslemelerini kullan
## Yapay Zekâ Destekli Tehdit Algılama <sup><sup>[1](https://x.com/NextDNS/status/1440291577713233925)</sup></sup>
> [!NOTE]
> NextDNS bu özelliği [beta](https://www.vocabulary.com/dictionary/beta) olarak etiketliyor, ancak çoğu kullanıcı iyi çalıştığını bildiriyor.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Yapay zekâ destekli tehdit algılamayı etkinleştir

## Google Güvenli Tarama <sup><sup> [1](https://safebrowsing.google.com/safebrowsing/report_general/) [2](https://blog.cryptographyengineering.com/2019/10/13/dear-apple-safe-browsing-might-not-be-that-safe/) [3](https://the8-bit.com/apple-proxies-google-safe-browsing-privacy/) [4](https://github.com/brave/brave-browser/wiki/Deviations-from-Chromium-(features-we-disable-or-remove)#services-we-proxy-through-brave-servers) </sup></sup>
> [!TIP]
> Bazı tarayıcılarda yerleşik olarak bulunan sürümün aksine, bu özellik genel IP adresinizi tehditlerle ilişkilendirmez ve engellemenin atlanmasına izin vermez. 

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Google Güvenli Tarama'yı etkinleştir

## Kripto Korsanlık (Cryptojacking) Koruması <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/cryptojacking.json)</sup></sup>
> [!CAUTION]
> [Önerilen blok listeleri](https://github.com/yokoffing/NextDNS-Config#privacy-lock) dışında bir şey kullanıyorsanız bu özelliği etkin bırakın (bkz. https://github.com/yokoffing/NextDNS-Config/issues/31).

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Kripto korsanlık korumasını etkinleştir

## DNS Rebinding Koruması <sup><sup>[1](https://help.nextdns.io/t/35hmval/what-is-dns-rebinding-protection) [2](https://www.reddit.com/r/nextdns/comments/t0ne8r/does_dns_rebinding_protection_block_remote_access/?context=3)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg)  DNS rebinding korumasını etkinleştir

## IDN Eşyazımı Saldırı Koruması <sup><sup>[1](https://web.archive.org/web/20230325073817/https://blog.riotsecurityteam.com/idn-homograph-attacksprevention) [2](https://akamai.com/blog/security/watch-your-step-the-prevalence-of-idn-homograph-attacks)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) IDN eşyazımı saldırı korumasını etkinleştir

## Yanlış Siteye Yönlendirme Koruması <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/typosquatting/protected-domains)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Yanlış siteye yönlendirme korumasını etkinleştir
## Alan Adı Oluşturma Algoritmaları (DGA) Koruması
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) DGA korumasını etkinleştir
## Yeni Kaydedilmiş Alan Adlarını (NRD'ler) Engelle <sup><sup>[1](https://boldgrid.com/instagram-influencer-accounts-are-being-hacked-phishing-attacks) </sup></sup>
> [!WARNING]
> NRD'leri engellemek [yanlış pozitiflere](https://csrc.nist.gov/glossary/term/false_positive) [bazen](https://www.reddit.com/r/InternetIsBeautiful/comments/w2wdro/comment/iguvg8y/?context=3) neden olabilir. NRD'leri izin listenize eklerken seçici olun; ve eğer eklerseniz, **ASLA** bir NRD'ye [hassas bilgi](https://egnyte.com/guides/governance/sensitive-information) vermeyin. *Yapılandırmanızı [kur ve unut](https://glosbe.com/en/en/set-and-forget) yapmayı planlıyorsanız, bu ayarı devre dışı bırakın.*

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Yeni kayıt edilmiş alan adlarını (NRD'ler) engelle

## Dinamik DNS Ana Bilgisayar Adlarını Engelle <sup><sup>[1](https://github.com/nextdns/ddns-domains/blob/main/suffixes) [2](https://x.com/NextDNS/status/1541740963760144386) </sup></sup>
> [!TIP]
> Dinamik DNS (DDNS) hizmetleri, bu ayarı kullandığınızda kendi web sitelerine erişmeye ve API'yi güncellemeye devam edebilir.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Dinamik DNS ana bilgisayar adlarını engelle

## Park Edilmiş Alan Adlarını Engelle <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/parked-domains-cname)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Park edilmiş alan adlarını engelle
## Üst Seviye Alan Adlarını (TLD'ler) Engelle <sup><sup>[1](https://webtribunal.net/blog/tld-statistics/) [2](https://www.spamhaus.org/reputation-statistics/cctlds/domains/) [3](https://bleepingcomputer.com/news/security/verified-twitter-accounts-hacked-to-send-fake-suspension-notices/) [4](https://github.com/DandelionSprout/adfilt/blob/master/Dandelion%20Sprout's%20Anti-Malware%20List.txt) [5](https://github.com/DandelionSprout/adfilt/issues/659#issuecomment-1284845803) </sup></sup>

> [!IMPORTANT]
> [TLD'leri](https://www.geeksforgeeks.org/components-of-a-url) engellemek, bu özellik hem site gezintilerini hem de alt istekleri durdurduğundan, kötü niyetli sitelerle birlikte yasal siteleri de engelleme riski taşır. Bununla birlikte, aşağıdaki girişler yaygın olarak kötüye kullanılan TLD'lere karşı koruma sağlarken günlük gezinmeye izin vermelidir.

<details><summary>TLD'leri görüntülemek için beni tıklayın</summary>

```
.autos
.best
.bid
.boats
.boston
.boutique
.charity
.christmas
.dance
.fishing
.hair
.haus
.loan
.loans
.men
.mom
.name
.review
.rip
.skin
.support
.tattoo
.tokyo
.voto
```

</details>

[Most Abused TLDs](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#tlds) adresinde ek girişler bulabilirsiniz, ancak zaman zaman siteleri [allowlist](https://github.com/yokoffing/NextDNS-Config#allowlist-white_check_mark) yapmanız gerekebilir. *Yapılandırmanızı [ayarla ve unut](https://glosbe.com/en/en/set-and-forget) yapmayı planlıyorsanız, bu adımı atlayın.*

## Çocukların Cinsel İstismarına İlişkin Materyalleri Engelle
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Çocukların cinsel istismarına ilişkin materyalleri engelle

***

# Privacy :lock:
Gizlilik özellikleri, şirketlerin hakkınızda toplayabileceği veri miktarını sınırlar.

Gizlilik bir [spektrum](https://blog.thenewoil.org/the-privacy-myth-binary-vs-spectrum) olduğundan, neye ihtiyacınız olduğu [tehdit modelinize](https://thenewoil.org/en/guides/prologue/threat-model/), ilgi alanınıza ve beceri setinize göre değişir.<sup>^[*neden önemsemeliyim? Saklayacak bir şeyim yok*](https://medium.com/@FabioAEsteves/i-have-nothing-to-hide-why-should-i-care-about-my-privacy-f488281b8f1d)</sup>

## Engelleme Listeleri <sup><sup>[1](https://github.com/nextdns/blocklists/tree/main/blocklists)</sup></sup>

Engelleme listeleri reklamları, [izleyicileri](https://www.freecodecamp.org/news/what-you-should-know-about-web-tracking-and-how-it-affects-your-online-privacy-42935355525/) ve kötü amaçlı siteleri filtreler. Yüzlerce gönüllü [open-source](https://opensource.com/resources/what-open-source) topluluğunda bu listelere katkıda bulunur ve onlar reklamları geniş ölçekte engellemeyi mümkün kılan gizli kahramanlardır.

NextDNS Ads & Trackers Blocklist](https://github.com/nextdns/blocklists/blob/main/blocklists/nextdns-recommended.json)'i **kaldırmanızı** ve [minimum](https://www.reddit.com/r/nextdns/comments/1048xeg/do_you_use_nextdns_blocklist_as_the_primary/j33wnz2/?context=3) sayıda yararlı listeyi **eklemenizi** öneririz.

### Hangi engelleme listesini kullanmalıyım?

Sorulması gereken harika bir soru şudur: “[Yanlış pozitiflerin](https://csrc.nist.gov/glossary/term/false_positive) rahatsızlıklarıyla ne kadar uğraşmak istiyorum?”

İşte geçmiş sorunlara ve gözlemlere dayanarak önerilen engelleme listeleri:

|     **Engelleme Listeleri**   |                              **Gerekçe**                                             |
|:--------------------:|:--------------------------------------------------------------------------------------:|
| HaGeZi - <br>Multi **NORMAL**<sup>[1](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#multi)</sup> <br>+ <br>OISD<sup>[2](https://www.reddit.com/r/nextdns/comments/1ia9bz0/comment/mdy61v9/)</sup> | İzleyici, reklam ve kötü amaçlı yazılım isteklerini sorunsuz bir şekilde engelleyin ([kur-ve-unut](https://glosbe.com/en/en/set-and-forget)). |
| HaGeZi - <br>Multi **PRO**<sup>[3](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#pro)</sup> | Genellikle sorunsuz bir şekilde daha fazla isteği engelleyin (önerilir)). |
| HaGeZi - <br>Multi **PRO++**<sup>[4](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#proplus)</sup> | Sitenin bozulması riskine karşı daha fazla isteği engelleyin. <br> [[şikayey](https://github.com/hagezi/dns-blocklists/issues/new/choose) edebilirsiniz ara sıra site ve uygulama sorunları. |

> [!TIP]
> Ayrı DNS profillerinde farklı engelleme listeleri kullanın (örneğin, yönlendiriciniz için NORMAL ve web tarayıcınız için PRO++).

Hagezi'nin kendi [tavsiyelerine](https://github.com/hagezi/dns-blocklists/tree/main#whatshouldiuse) de göz atabilirsiniz.

### Neden Hagezi?
[Hagezi](https://github.com/hagezi/dns-blocklists) reklamları, izleyicileri, yerel cihaz izleyicilerini ve kötü amaçlı yazılımları engeller. Mantıklı bir izin listesi tutar, yanlış pozitifleri hızlı bir şekilde ele alır ve bilinen sorunları engelleme listelerini koruyanlara iletir. Hagezi'nin birincil DNS listeleri, [OISD](https://oisd.nl/), [Steven Black](https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts), [1Hosts](https://github.com/badmojr/1Hosts#safeguard-your-devices-against-pesky-ads-trackers-and-malware), [notrack](https://gitlab.com/quidsup/notrack#notrack) ve [bir çogu](https://github.com/hagezi/dns-blocklists/blob/main/sources.md) gibi saygın topluluk engelleme listeleri dahil olmak üzere birden fazla [kaynak](https://github.com/hagezi/dns-blocklists/wiki/FAQ#-which-sources-are-used-for-the-lists-and-how-are-the-lists-compiled-on-the-basis-of-these-sources) birleştirir.

Diğer listelerin neden kullanılmadığını da merak edebilirsiniz. Bunun nedeni birçok liste yöneticisinin:
* [Yanlış pozitifleri](https://csrc.nist.gov/glossary/term/false_positive) kaldırmayan ve/veya artık aktif olmayan <sup>[1](https://github.com/lightswitch05/hosts/issues/356) [2](https://github.com/EnergizedProtection/block/issues/916)</sup>
* zaten [toplu](https://www.reddit.com/r/nextdns/comments/ys3s1s/confused_about_blocklists/ivxdcd2/?context=3) ortak engelleme listelerini kendi listelerine (Easylist/Fanboy, AdGuard, Steven Black, vb.) <sup>[1](https://github.com/badmojr/1Hosts/blob/master/-data/lists/assets.txt) [2](https://oisd.nl/includedlists/big/0) [3](https://github.com/jerryn70/GoodbyeAds/blob/master/Docs/Sources.md) [4](https://github.com/hagezi/dns-blocklists/blob/main/sources.md#sources) </sup>
* Yukarıdaki tablo kombinasyonları ile karşılaştırıldığında anlamlı bir ek koruma sağlamaz.

## Yerel İzleme Koruması <sup><sup>[1](https://github.com/nextdns/native-tracking-domains/tree/main/domains)</sup></sup>

Kullandığınız tüm cihaz markalarını ekleyin.

<details>

	Windows
	Apple
	Samsung
	Xiaomi
	Huawei
	Amazon Alexa
	Roku
	Sonos

</details>

## Gizlenmiş Üçüncü Taraf İzleyicileri Engelle <sup><sup>[1](https://github.com/nextdns/cname-cloaking-blocklist/blob/master/domains) [2](https://www.reddit.com/r/nextdns/comments/10nenu3/disguised_trackers_are_blocked_regardless_of) [3](https://medium.com/nextdns/cname-cloaking-the-dangerous-disguise-of-third-party-trackers-195205dc522a) [4](https://arxiv.org/pdf/2102.09301.pdf) [5](https://tma.ifip.org/2020/wp-content/uploads/sites/9/2020/06/tma2020-camera-paper66.pdf) </sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Gizlenmiş üçüncü taraf izleyicileri engelle

## Ortaklık ve İzleme Bağlantılarına İzin Ver <sup><sup>[1](https://github.com/nextdns/click-tracking-domains) [2](https://x.com/NextDNS/status/1539229377560461312) </sup></sup>
> [!TIP]
> Gizliliğinizi korumak için IP adresiniz otomatik olarak gizlenecektir ([TCP](https://educba.com/what-is-tcp-ip) [proxying](https://en.wikipedia.org/wiki/Proxy_server#/media/File:Proxy_concept_en.svg) aracılığıyla).<p>

> [!WARNING]
> Bu ayarın devre dışı bırakılması bazı e-posta bağlantılarının düzgün açılmasını engeller.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Ortaklık ve izleme bağlantılarına izin ver

***

# Ebeveyn Kontrolü :family_man_woman_boy:
## YouTube Kısıtlı Modu
![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) YouTube Kısıtlı Mod'u zorunlu kıl
## Atlatma Yöntemlerini Engelle <sup><sup>[1](https://github.com/nextdns/dns-bypass-methods)</sup></sup>
VPN'ler, proxy'ler, Tor yazılımı ve şifreli DNS hizmetleri gibi NextDNS filtrelemesini atlayabilecek araçları engelleyin.
> [!CAUTION]
> Bu ayarın etkinleştirilmesi istenmeyen davranışlara neden olur.

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Atlatma yöntemlerini engelle
***

# Kara Liste :no_entry:

Denylist girişleri her zaman engellenir. Bu girişler, günlük taramayı engellemeden bazı profilleri daha da zorlaştırabilir.

### iCloud Private Relay

[iCloud Private Relay](https://support.apple.com/en-us/102602) cihazlardaki DNS ayarlarını geçersiz kılarak NextDNS'in onları korumasını engelleyebilir.

Bazı DoH sağlayıcıları bu özelliği otomatik olarak engeller.

	mask.icloud.com
	mask-h2.icloud.com
	mask-canary.icloud.com

Ve muhtemelen:

  	apple-relay.cloudflare.com
    apple-relay.fastly-edge.com
	doh.dns.apple.com
	doh.dns.apple.com.v.aaplimg.com
    mask-api.icloud.com
    mask.apple-dns.net

***

# Beyaz Liste :white_check_mark:

İzin listesi girdileri her zaman çözümlenir. Bu girdiler, agresif DNS profillerinin kurallarını gevşetmesi için gerekli olabilir.

### NextDNS

Bir filtre listesinin [haywire](https://help.nextdns.io/t/m1hs207/energized-ultimate-lists-blocking-nextdns) gidip erişiminizi engellemesi durumunda NextDNS'in kendisine izin verin.

	nextdns.io

<details><summary>Daha çok girdi görmek için bana tıkla</summary>

### Facebook / Instagram <sup><sup>[1](https://github.com/jerryn70/GoodbyeAds/issues/309)</sup></sup> 

	graph.facebook.com
	graph.instagram.com
	i.instagram.com
	b-graph.facebook.com

Eğer hala sorun yaşıyorsan, [bunları](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/share/facebook.txt) dene:
	
	connect.facebook.com
	connect.facebook.net
	graph-fallback.facebook.com
	z-m-graph.facebook.com
	graph-fallback.instagram.com

### Apple cihaz güncellemeleri <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/536) [2](https://github.com/badmojr/1Hosts/issues/562) [3](https://github.com/nextdns/metadata/pull/1132#issuecomment-1331733770)

Bir [bilinen izleme alanı](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558), ancak cihaz güncellemeleri için gereklidir.

	xp.apple.com

### Apple iMessage GIFs <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/560)</sup></sup> / Spotlight aramam <sup><sup>[2](https://github.com/badmojr/1Hosts/issues/562)</sup></sup> 

	smoot.apple.com

### Apple Store <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/xx4cwn/solutionapple_store_connection_issues)</sup></sup> 

	amp-api-edge.apps.apple.com
	amp-api-search-edge.apps.apple.com

### Windows

Bu [istek](https://oisd.nl/excludes.php?w=settings-win.data.microsoft.com) NextDNS'in [Yerel İzleme](https://github.com/yokoffing/NextDNS-Config#native-tracking-protection-1) listesi kullanılırken engelleniyor (Windows)

	settings-win.data.microsoft.com

### Xbox başarımları

	v10.events.data.microsoft.com
	v20.events.data.microsoft.com

### Xiaomi cihaz güncellemeleri

	update.intl.miui.com

### Xiaomi USB hata ayıklama (Güvenlik ayarları)

	srv.sec.intl.miui.com

### Google Nest kullanım metrikleri <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/yzvnuw/nest_usage_metrics_being_blocked)</sup></sup> 

	logsink.devices.nest.com

### Yahoo Mail <sup><sup>[1](https://github.com/hagezi/dns-blocklists/issues/269)</sup></sup>

	consent.yahoo.com
	guce.oath.com
	pr.comet.yahoo.com

### [Spectrum](https://spectrum.net) login <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/640)</sup></sup>

	pov.spectrum.net

### Zoom <sup><sup>[1](https://oisd.nl/excludes.php?w=log.zoom.us) [2](https://oisd.nl/excludes.php?w=us04logfiles.zoom.us)</sup></sup> 

	logfiles.zoom.us
	us04logfiles.zoom.us
	us04zpns.zoom.us

### YouTube geçmiş

	s.youtube.com

### Hulu <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/762)</sup></sup>

	ads-fa-darwin.hulustream.com

### Epic Games Launcher <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/643)</sup></sup>

	eulatracking-public-service-prod06.ol.epicgames.com

### NVIDIA Gefore Experience <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/650)</sup></sup>
	
	gfe.nvidia.com
	nvgs.nvidia.cn

### Chick-Fil-A App <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/zaqio0/comment/iz7v9di/?utm_source=share&utm_medium=web2x&context=3)</sup></sup>

	tmetrix.my.chick-fil-a.com

### [imgur](https://imgur.com) <sup><sup>[1](https://github.com/lightswitch05/hosts/issues/358) [2](https://www.reddit.com/r/nextdns/comments/t3jmvk/imgur_loads_then_goes_blank_no_matter_which)</sup></sup>

	js.media-lab.ai

### [CBS](https://cbsnews.com/live) News livestream <sup><sup>[1](https://github.com/nextdns/metadata/issues/1030) [2](https://github.com/hagezi/dns-blocklists/issues/422)</sup></sup> 

	doppler-config.cbsivideo.com
	production-cmp.isgprivacy.cbsi.com
	pubads.g.doubleclick.net
	tags.tiqcdn.com 

### [Paramount+](https://www.paramountplus.com/)

Paramount+ reklamları görüntülemek için belirli etki alanlarını kullanır. Paramount+ içeriğinin yüklenebilmesi için bu alan adlarının erişilebilir olması gerekir (reklamsız planlara sahip izleyiciler için bile).

Uyarı: Ancak, birçok site bu etki alanlarını reklamlar için kullandığından, bunlara izin vermek ziyaret ettiğiniz diğer sitelerde daha fazla reklam gösterilmesine neden olabilir.

    imasdk.googleapis.com
    pubads.g.doubleclick.net

Kullanıcılar aşağıdaki alan adlarına da izin verilmesi gerekebileceğini [bildirmişlerdir](https://www.reddit.com/r/nextdns/comments/v84ag6/paramount_plus/):

    cbsaavideo.com
    cbsi.com
    conviva.com
    convivia.com
    demdex.net
    dns-clientinfo.cbsivideo.com
    partnerad.l.doubleclick.net
    saa.cbsi.com
    summerhamster.com (yes, really)
    udm.scorecardresearch.com

### [FiveThirtyEight](https://fivethirtyeight.com) videos / [National Geographic](https://nationalgeographic.com) website <sup><sup>[1](https://github.com/notracking/hosts-blocklists/issues/788)</sup></sup>

	dcf.espn.com

### [Men's Health](https://menshealth.com/nutrition/a40868905/chris-hemsworth-chicken-pasta-bake-recipe-centr) videos <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/651)</sup></sup>

	glimmer.hearstapps.com

</details>

***

# Ayarlar :gear:

## Günlükler
**Depolama konumu** → İsviçve

## Engel Sayfası
> [!CAUTION]
> [NextDNS Root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) cihazlarınızda yoksa bu ayarın etkinleştirilmesi sitede gezinme sorunlarına neden olabilir. Ayrıca, bu ayar [Paypal 2FA](https://github.com/hagezi/dns-blocklists/issues/2335), [iCloud Private Relay](https://help.nextdns.io/t/g9hdska), [Microsoft Teams](https://www.reddit.com/r/nextdns/comments/176u2x6/comment/k4pp3ti/?context=3), [Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343), NAVER uygulaması, [Hoyolab uygulaması](https://help.nextdns.io/t/g9yxqcd/nextdns-blocking-hoyolab) ve muhtemelen [bankacılık uygulamaları](https://help.nextdns.io/t/83yxjgx/most-common-problem-with-nextdns)'nı bozar.

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Engel sayfasını etkinleştir

## Anonimize EDNS İstemci Alt Ağı <sup><sup>[1](https://help.nextdns.io/t/m1hmv04/what-is-edns-client-subnet-ecs) </sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Anonimize EDNS İstemci Alt Ağı'nı etkinleştir
## Önbellek Arttırma <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/girmcf/new_setting_cache_boost/)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Önbellek arttırmayı etkinleştir

## CNAME Düzleştirme <sup><sup>[1](https://medium.com/nextdns/nextdns-added-cname-uncloaking-support-becomes-the-first-cross-platform-solution-to-the-problem-e3f437f84342) [2](https://developers.cloudflare.com/dns/cname-flattening/) [3](https://advancedweb.hu/what-is-cname-flattening-and-how-it-helps-redirecting-the-apex-domain) </sup></sup>
> [!WARNING]
> Bu özelliğin etkinleştirilmesi [Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343) ile uyumluluğu bozabilir ve belirli engelleme listelerinde sorunlara neden olabilir.

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) CNAME düzleştirmeyi etkinleştir

## Web3 <sup><sup> [1](https://x.com/NextDNS/status/1491034351391305731) [2](https://gabygoldberg.notion.site/f7050e62461143d49345e7b46eb5576b)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Web3'ü etkinleştir → (isteğe bağlı)

***
# SSS :question:

## NextDNS'e nasıl kaydolabilirim?
Başlamak için [buraya](https://nextdns.io/?from=xujj63g5) tıklayın

## Neden hala reklam görüyorum?
Tüm reklamlar DNS düzeyinde engellenemez.<sup>[1](https://www.reddit.com/r/nextdns/comments/14nsfhv/comment/jq982bi/?context=3) [2](https://www.reddit.com/r/nextdns/comments/13urdda/ads_on_manga_sites/)</sup> Arta kalanları engellemek için bir [reklam engelleyiciye](https://github.com/yokoffing/NextDNS-Config#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) ihtiyacınız olacak.

Bunun nedeni, tüm reklamların üçüncü taraf alan adlarından gelmemesidir; [YouTube](https://discourse.pi-hole.net/t/how-do-i-block-ads-on-youtube/253/2) gibi bazı reklamlar doğrudan ziyaret ettiğiniz siteden gelir. DNS engelleyiciler bir alan adının çözümlenmesini durdurur ve içerik engelleyiciler sayfa içeriğini filtreler. Hafif bir reklam engelleyiciyi kolayca yüklemek için [buraya](https://github.com/yokoffing/NextDNS-Config/tree/main#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) tıklayın.

## Reklam engelleme özelliğine sahip bir tarayıcıya ihtiyacım var. Hangisini seçmeliyim?
Bir tarayıcı seçmek [başlangıç Pokémon'unu seçmek](https://www.youtube.com/watch?v=F_8htiBjTCY) kadar samimidir, bu yüzden burada birkaç uyarı var:
* Kağıt üzerindeki en iyi tarayıcı gerçek dünya kullanımında iyi çalışmayabilir.
* Tarayıcılar birer araçtır! Ne yapmanız gerektiğine bağlı olarak çeşitli tarayıcılar kullanın.
* Yaşamın farklı alanları (örn. iş, okul, kişisel) için çeşitli tarayıcılar (veya tarayıcı profilleri) kullanmalısınız.


Aşağıdaki önerileri etkinlik, kaynak verimliliği, özellikler ve kullanım kolaylığının bir kombinasyonuna dayandırdık
Reklam engelleme özelliğine sahip bir tarayıcıya ihtiyacım var. Hangisini seçmeliyim?
Bir tarayıcı seçmek [başlangıç Pokémon'unu seçmek](https://www.youtube.com/watch?v=F_8htiBjTCY) kadar samimidir, bu yüzden burada birkaç uyarı var:
* Kağıt üzerindeki en iyi tarayıcı gerçek dünya kullanımında iyi çalışmayabilir.
* Tarayıcılar birer araçtır! Ne yapmanız gerektiğine bağlı olarak çeşitli tarayıcılar kullanın.
* Yaşamın farklı alanları (örn. iş, okul, kişisel) için çeşitli tarayıcılar (veya tarayıcı profilleri) kullanmalısınız.

| İşletim sistemi | Tarayıcı | İçerik Engelleyici |
|---|---|---|
| iOS | [Safari](https://www.privacyguides.org/en/mobile-browsers/#safari) | [AdGuard](https://www.privacyguides.org/en/browser-extensions/?h=adguard#adguard) |
| Android | [Brave](https://www.privacyguides.org/en/mobile-browsers/#brave) | Dahili engelleyici |
| Windows <br> macOS <br> Linux | [Firefox](https://www.mozilla.org/en-US/firefox/new/) (with [Betterfox](https://github.com/yokoffing/Betterfox#betterfox)) <p><p> [Brave](https://www.privacyguides.org/en/desktop-browsers/#brave) | [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) <p><p> Dahili engelleyici veya [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) |  |

Günün sonunda, [NextDNS](https://nextdns.io/?from=xujj63g5) + reklam engelleyicili herhangi bir tarayıcı kullanıyorsanız, çoğu insandan daha fazla kapsama alanına sahipsiniz demektir.

## NextDNS için ödeme yapmalı mıyım?
Sağladığı zengin özellikler için [NextDNS](https://nextdns.io/?from=xujj63g5) sınırsız cihaz için 19,90 $/yıl ile çok uygun. NextDNS ailemi kötü niyetli bir olaydan kurtarırsa kendini amorti eder.

## Etkinleştirilen özelliklerin miktarı NextDNS'in hızını etkiliyor mu?<sup>[1](https://github.com/yokoffing/NextDNS-Config/issues/12#issue-1465457977) [2](https://www.reddit.com/r/nextdns/comments/135utai/comment/jilbus8/?=&context=3)</sup>

Açtığınız ayarların sayısı DNS gecikmenizi etkilemeyecektir.

## NextDNS'i sistem düzeyinde zaten kullanıyorsam DoH'u tarayıcı düzeyinde ayarlamam gerekir mi??
Tarayıcı için ayrı bir profil kullanmadığınız sürece, [gerekli değil](https://www.reddit.com/r/nextdns/comments/yfjvqy/is_it_redundant_to_set_at_doh_at_browserlevel_if/iu3vjzt/?context=3). Ancak, [web tarayıcınızda ayarlamanızı](https://itechtics.com/dns-over-https/#how-to-enable-or-disable-dns-over-https-in-your-browsers) yine de tavsiye ederim. 

## Bir yönlendirici profiline ve bir cihaz profiline sahibim. Cihazım hangisini kullanıyor?
Cihaz [NextDNS](https://nextdns.io/?from=xujj63g5) uygulaması veya yüklü [root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) tarafından ayarlanan profili kullanacaktır. Ancak, cihaz ayrı bir profil kullanacak şekilde yapılandırılmamışsa, wifi/yönlendirici yapılandırmasını kullanır.<sup>[1](https://www.reddit.com/r/nextdns/comments/yf4hnv/question_about_home_router_and_app_running_in/)</sup>

## Güvenlik, gizlilik ve anonimlik arasındaki fark nedir?
[makale](https://guvendekal.org/#/mahremiyet?id=mahremiyet-g%c3%bcvenlik-ve-anonimlik) | [video](https://youtu.be/MJ-ekgoQrOM?si=p3KHhcCG6suteXfS&t=70)

## NextDNS, İnternet Servis Sağlayıcımdan (İSS) gelen etkinlikleri gizliyor mu?
Şifrelenmiş DNS sorguları gizliliği ve güvenliği artırır. Bu şifreleme, İSS'nizin hangi web sitelerini aradığınızı ve ziyaret ettiğinizi görmesini engeller.


Ancak şifrelenmiş DNS, web sitesi IP adreslerini İSS'nizden gizlemez. İSS'niz erişmek istediğiniz belirli etki alanını göremese de Cloudflare veya AWS gibi DNS sunucularına başvurduğunuzu görebilir. Belirli bir IP adresine tekrar tekrar veri gönderirseniz, İSS'niz bu adresteki bir web sitesini ziyaret ettiğinizi tahmin edebilir.
Şifrelenmiş DNS sorguları gizliliği ve güvenliği artırır. Bu şifreleme, İSS'nizin hangi web sitelerini aradığınızı ve ziyaret ettiğinizi görmesini engeller.

## VPN'e ihtiyacım var mı?
IVPN [argues](https://www.ivpn.net/blog/why-you-dont-need-a-vpn/) sadece üç nedenden dolayı bir VPN'e ihtiyacınız vardır. Temel olarak, aşağıdakiler için


1. Gerçek IP adresinizi web sitelerinden ve eşler arası ağlardan gizleyerek İSS'lerin ve mobil operatörlerin çevrimiçi etkinliğinizi izlemesini önler.


2. [ortadaki adam](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) ve diğer [yaygın saldırılar](https://en.wikipedia.org/wiki/Evil_twin_(wireless_networks)) havaalanları, oteller, kafeler ve kütüphaneler gibi yerlerdeki halka açık Wi-Fi ağlarına.


3. Sansürü veya coğrafi kısıtlamaları atlayarak engellenen web sitelerine ve içeriğe erişmenizi sağlar.

Sonuç olarak, [tehdit modeliniz](https://thenewoil.org/en/guides/prologue/threat-model/) gerektirmediği sürece bir VPN'e ihtiyacınız yoktur. İşte [Techlore](https://www.techlore.tech/vpn.html) ve [Tom Spark Reviews](https://www.vpntierlist.com/vpn-tier-list-2024)'den VPN önerileri.

***
# Bahsedenler :books:

### Kullanıcı Yorumları
* [buraya bakın](https://socialgrep.com/search?query=yokoffing%2Cnextdns)

### YouTube
* [The ULTIMATE Guide to Mastering NextDNS!](https://www.youtube.com/watch?v=WUG57ynLb8I&t=2230s) | [clarifications](https://github.com/techlore/channel-content/issues/43) (July 2023) 

### makaleler
* [Knot Resolver — with ad blocking](https://blog.cavelab.dev/2022/12/knot-resolver-ad-blocking/) (Dec 2022)
* [Privacy Toolkit: NextDNS](https://stephenbolen.com/privacy-toolkit-nextdns/#:~:text=I%20found%20a%20wonderful%20guide%20on%20GitHub%20that%20walks%20through%20the%20optimal%20NextDNS%20configuration) (Sept 2022)

### Rehberler
* [A comprehensive guide to setting up NextDNS](https://itsjake.me/blog/a-comprehensive-guide-to-setting-up-nextdns/) (Sept 2023)
* [FMHY: DNS Adblocking](https://github.com/nbats/FMHYedit/blob/main/AdblockVPNGuide.md#-dns-adblocking) → NextDNS → Guide
* [hagezi/dns-blocklists](https://github.com/hagezi/dns-blocklists#department_store-nextdns---limited-freepaid-) → Online DNS Services

### Katkıda Bulunanlar
* [Hagezi](https://github.com/hagezi/dns-blocklists/issues?q=author%3Ayokoffing) | [mentions](https://github.com/hagezi/dns-blocklists/issues?q=mentions%3Ayokoffing)
* [1Hosts](https://github.com/badmojr/1Hosts/issues?q=author%3Ayokoffing)
* [Easylist](https://github.com/easylist/easylist/issues?q=author%3Ayokoffing)
* [uBlock Origin](https://github.com/uBlockOrigin/uAssets/issues?q=author%3Ayokoffing)
* [AdGuard](https://github.com/AdguardTeam/AdguardFilters/issues?q=author%3Ayokoffing)

<div align='center'><a href='https://websitecounterfree.com'><img src='https://websitecounterfree.com/c.php?d=9&id=19651&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>since 23 July 2022</div>
