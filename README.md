# socketprogram
Bir soket, ağ üzerinden çalışan iki program arasındaki iki yönlü bir iletişim bağlantısının bir uç noktasıdır. Ağ üzerinden çalıştırma, programların genellikle yerel ve uzak bilgisayarlar olarak adlandırılan farklı bilgisayarlarda çalışması anlamına gelir.

Sunucu ile iletişim için bir soket oluşturduğunda bir istemci programı tarafından bir ağ bağlantısı başlatılır. Java'da soketi oluşturmak için istemci Socket yapıcısını çağırır ve sunucu adresini ve belirli sunucu bağlantı noktası numarasını ona iletir. Bu aşamada, sunucu belirtilen adrese sahip ve belirli port numarasındaki bağlantıları dinleyen makinede başlatılmalıdır.
Sunucu, yalnızca istemcilerden gelen bağlantı isteklerini dinlemeye adanmış belirli bir bağlantı noktası kullanır. İstemci ile veri iletişimi için bu belirli bağlantı noktasını kullanamaz, çünkü sunucunun herhangi bir anda istemci bağlantısını kabul edebilmesi gerekir. Bu nedenle, özel bağlantı noktası yalnızca yeni bağlantı isteklerini dinlemeye adanmıştır. Belirli bir bağlantı noktasıyla ilişkili sunucu tarafı soketine sunucu soketi denir. Bu sokete istemci tarafından bir bağlantı talebi geldiğinde, istemci ve sunucu bir bağlantı kurar. 

Bu bağlantı şu şekilde kurulur:

⦁	Sunucu, belirli bir sunucu portunda bir bağlantı isteği aldığında, bunun için yeni bir soket oluşturur ve bir port numarasını ona bağlar.
⦁	Bağlantının kurulduğunu bildirmek için yeni port numarasını müşteriye gönderir.
⦁	Sunucu şimdi iki port dinleyerek devam ediyor:
⦁	belirli bağlantı noktasında yeni gelen bağlantı isteklerini bekler ve
⦁	Kabul edilen müşteri ile kurulan bağlantıda (yeni limanda) mesaj okur ve yazar.
