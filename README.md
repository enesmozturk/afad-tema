# afad-tema
 Pardus yüklü PC lerde kurumsal yapı oluşturmak için masaüstü arka plan resimlerini ve login arkafon resimlerini değiştiren paket kodu
## İçindekiler:
    * Varsayılan resimlerin bulunduğu klasöre resimleri yüklemek
    * Arkaplan resmini değiştirmiş olanlarında ayarları sıfırlamak
## Komutlar:
### Yeni Kullancılar
    * Ayarları varsayılan olacağı için komuta ihtiyaç yok
### Var Olan Kullanıcılar
    * #######Kullanicilarin ayarlarini duzeltiyor###########
        find /home -type f -name "xfce4-desktop.xml" -print0 | xargs -0 sed -i 's+name="last-image" type="string".*+name="last-image" type="string" value="/usr/share/images/desktop-base/default"/>+g'
    * ######olceklendırme fil olmasini sagliyor##############
        find /home -type f -name "xfce4-desktop.xml" -print0 | xargs -0 sed -i 's+name="image-style" type="int".*+name="image-style" type="int" value="3"/>+g'
