---
title: Tekrar eden satınalma siparişi oluşturma
description: Bu makale önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608124"
---
# <a name="create-a-repeat-purchase-order"></a>Tekrar eden satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu makale önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir. Tekrar eden siparişleri oluşturmak için iki yöntem vardır. Eylem Bölmesi'nden belge düzeyindeki kullanılabilir eylemleri kullanabilir veya satır ayrıntısı eylemlerini kullanabilirsiniz. Belge düzeyindeki eylemler, başka bir siparişten satırlar ve başlık bilgileri ekleyerek yeni bir satınalma siparişi oluşturmak ve satır ayrıntıları eylemi ise temel olarak mevcut bir siparişe satır eklemek içindir. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Bu görev genellikle bir satınalma temsilcisi tarafından gerçekleştirilir.

## <a name="create-a-new-repeat-purchase-order"></a>Yeni bir tekrar eden satınalma siparişi oluşturun

1. Gezinti bölmesinde **Modüller \> Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri** ne gidin. İlk olarak bilgileri yeni siparişe kopyalama seçeneğini deneyeceğiz.  
1. **Yeni**'yi seçin.
1. **Satıcı hesabı** alanına `US-101` girin.
1. **Tamam**'ı seçin.
1. Eylem bölmesinde **Satınalma siparişi** sekmesini açın ve **Kopyala** grubundan **Tümünden**'i seçin. **Diğer belgelerden kopyala** iletişim kutusu açılır. Buradan, mevcut siparişlerinizden siparişinize kopyalayabilirsiniz. Satırların nasıl kopyalandığına ilişkin farklı seçenekler ve kopyalama yapabileceğiniz farklı belge türleri vardır. İlk olarak satırların nasıl kopyalanacağını inceleyeceğiz.
1. **Parametreler** hızlı sekmesini genişletin.

    - **Miktar faktörü** alanı, kopyalama yaptığınız sırada açık olandan farklı bir miktar kullanmanız gerekiyorsa yararlıdır. Örneğin; kopyaladığınız satırlardaki miktarı iki kez sipariş etmek isterseniz bu alana '2' yazarsınız ve sonra sistem orijinal miktarın ikiye katlandığı yere satır ekler.  
    - **İşareti tersine çevir** alanı da eklenen sipariş satırları için miktarın işaretini değiştirerek sipariş edilen miktarı değiştirmeyi destekler. Bu, hareketi iptal eden sipariş satırları oluşturularak hareketi tersine çevirmeniz gerektiğinde yararlı olabilir. Bu seçenek, sayfa **Alacak dekontu oluştur** eyleminde açıldığında otomatik olarak seçilir.  
    - **Masrafları kopyala** seçeneği, masrafları sipariş satırlarını kopyaladığınız belgedeki yeni siparişinize kopyalamanızı sağlar.  
    - **Fiyatları yeniden hesapla** seçeneği bunları diğer bilgileri kopyaladığınız belgeden kopyalamak yerine geçerli fiyatları ve indirimleri kullanır.  
    - **Tam olarak kopyala** seçeneği, sipariş başlığı ve satırlarındaki çeşitli alanların değerlerini kopyalar. Bu seçenek belirlenmezse yeni siparişi el ile oluşturuyormuş gibi satıcı ve ürünlerle ilgili birçok alan için varsayılan değerler kullanılır. Örneğin, **Tam olarak kopyala** seçeneğini *Evet* olarak ayarlar ve satıcı için varsayılan fatura hesabını geçersiz kılan bir siparişi kopyalarsanız aynı fatura hesabı yeni siparişinize kopyalanır. **Tam olarak kopyala** seçeneğini *Hayır* olarak ayarlarsanız bunun yerine yeni siparişinizde satıcı için varsayılan fatura hesabı kullanılır. **Tam olarak kopyala** seçeneği *Evet* olarak ayarlandığında aşağıdaki alanların değerleri kopyalanır:
        - Dil
        - Ödeme koşulları
        - Ödeme yöntemi
        - Ödeme belirtimi
        - Numara serisi grubu
        - Nakit iskontosu
        - İskonto yüzdesi
        - Para birimi
        - Teslimat koşulları
        - Teslimat şekli
        - Boyut
        - Satış vergi grubu
        - Satış vergisini geçersiz kıl
        - Fiyatlara satış vergisi dahildir
        - Taşıma
        - Liman
        - İstatistik prosedürü
        - Şablon kodu
        - Teslimat adı
        - Posta adresi
        - Referans
        - Referans Tablosu Kodu
    - **Satınalma satırlarını sil** seçeneği, yeni satırları uygulamadan önce kopyaladığınız satınalma siparişinde halihazırda var olan tüm satınalma siparişi satırlarını siler. Uyarı vermeden mevcut tüm satırları sildiğinden bu seçeneği dikkatli kullanın.  
    - **Sipariş başlığını kopyala** seçeneğini kullanırsanız yeni siparişinizde başlık bilgilerini el ile oluşturmanız gerekmez. Bu seçenek, satıcıyla ilişkili alanlar için varsayılan değerlerin kullanılmasına neden olur. Kopyalama yaptığınız belgede kopyalamak istediğiniz varsayılan olmayan değerler varsa **Tam olarak kopyala** seçeneği de kullanın.
    - Kopyalama yapabileceğiniz farklı belge kaynakları vardır ve her biri bu sayfa üzerinde ayrı bir bölüme sahiptir. Örneğin, **Satın alma siparişleri** bölümü mevcut satınalma siparişlerinden kopyalama yapmanızı sağlar.  

1. **Satınalma siparişleri** bölümünde, panonuza kopyalanmasını istediğiniz satırları seçin. Diğer satınalma siparişlerinden ek satınalma siparişi satırlarının seçilmesi ve bunların siparişinize kopyalanması mümkündür. Satınalma belgelerinin diğer türlerinden de satır eklemek mümkündür. Sonraki birkaç adımda farklı seçenekler gözden geçirilir.  
1. **Onay** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için satınalma siparişi onaylarını buradan seçebilirsiniz. Satınalma siparişi onayları ilişkili satınalma günlüğü kimliği veya satınalma siparişi kimliği ile tanımlanır.  
1. **Ürün girişleri** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için ürün girişi günlüklerini buradan seçebilirsiniz. Ürün girişi günlükleri ürün giriş fişi veya satınalma siparişi kimliği ile tanımlanır.
1. **Faturalar** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için satıcı faturalarını buradan seçebilirsiniz. Faturalar, fatura fişi veya satınalma siparişi kimliğiyle tanımlanır.
1. **Seçilen satırlar veya kopyalanacak başlık** bölümünü genişletin. Bu görünüm siparişinize kopyalamak için seçilmiş tüm belgeler ve satırların özetini gösterir.
1. **Tamam**'ı seçin. Seçtiğiniz satır yeni satınalma siparişinize kopyalandı.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Satırları mevcut satınalma siparişine kopyalayın  

Siparişin tamamını kopyalamak yerine yeni bir PO oluşturmak, PO başlığındaki bilgileri tamamlamak ve sonra mevcut siparişlerden tek tek satırları kopyalamak daha yaygın bir uygulamadır.  

1. **Satın alma siparişi** satırını seçin.
1. **Tümünden**'i seçin. Sayfa önceden görüntülenenin aynısını açar ancak sipariş satırlarını görünümünden açıldığında farklı seçenekler seçilir. Parametreleri gözden geçirelim.
1. **Parametreler** bölümünü genişletin.

    - **Satınalma satırlarını sil** seçeneği belirlenmez. Bu, mevcut satırları kaldırmadan siparişinize yeni satırlar kopyalayabileceğiniz anlamına gelir.
    - Siparişe yalnızca ek satırlar eklediğimizden **Sipariş başlığını kopyala** seçeneği de seçilmez.
    - Bu örnekte, mevcut satınalma siparişinden satırları kopyalayacağız.

1. İstenen satınalma emri için satırı seçin. Bu PO üzerinde tek sipariş satırının da seçildiğine dikkat edin.  
1. **Tamam**'ı seçin. Ek sipariş satırı satınalma siparişinize eklendi.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]