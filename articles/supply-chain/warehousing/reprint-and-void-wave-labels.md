---
title: Dalga etiketlerini yeniden yazdırma ve hükümsüz kılma
description: Bu konu, mevcut dalga etiketlerinin nasıl hükümsüz kılınacağını ve yeniden yazdırılacağını açıklamaktadır.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: af92334af28824b3fcebde5f046bd7c6da459885
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016666"
---
# <a name="reprint-and-void-wave-labels"></a>Dalga etiketlerini yeniden yazdırma ve hükümsüz kılma

[!include [banner](../includes/banner.md)]

Bu konu, dalga işleme tarafından oluşturulan etiketlerin nasıl yönetileceğini açıklar. (Ayrıntılı açıklama ve yapılandırma yönergeleri için bkz. [Dalga etiketi yazdırmayı yapılandırma](../warehousing/configure-wave-label-printing.md).)

Dalga etiketlerini istediğiniz zaman yeniden yazdırabilirsiniz. Örneğin, mevcut bir etiket kaybedildiyse veya zarar gördüyse tek bir etiketi yazdırmanız gerekebilir. Alternatif olarak, tam bir dalga etiketi serisinin numarası ve/veya kompozisyonu (örneğin, stok yetersizliği veya başka nedenlerle) değişirse, bir ambar çalışanı veya gözetmen tüm etiketleri yeniden yazdırmak zorunda kalabilir. Genellikle, yalnızca kartonlar değişse bile, her bir etiketin "Koli X / Y" bölümünde doğru toplam sayıyı korumak için tüm rulonun yeniden yazdırılması gerekebilir.

Dalga etiketlerini yeniden yazdırma özelliği aşağıdaki işlevleri destekler:

- Etiketleri hem ambarlama uygulaması hem de zengin istemciden yeniden yazdırma.
- Etiketleri hükümsüz kılma ve eş zamanlı olarak yeniden yazdırma. (Örneğin, etiketleri hükümsüz kılma özelliği eksik çekme senaryolarına katıştırılmıştır.)
- Dalga etiketi geçmişini temizleme.

Bu konu, örnekler aracılığıyla, dalga etiketlerini yeniden yazdırma özelliğinin nasıl kullanılacağını gösteren bir dizi senaryoyu göstermektedir.

> [!IMPORTANT]
> Bu konuda sunulan senaryolarda çalışmak için, öncelikle [Dalga etiketi yazdırmayı yapılandırma](../warehousing/configure-wave-label-printing.md) bölümünde açıklandığı gibi ilgili dalga yazdırma özelliklerini açmanız ve yapılandırmanız gerekir. Bu konudaki senaryoların bazıları, önkoşul olarak gerekli örnek verileri oluşturmak için öncelikle ilgili konudaki senaryolar aracılığıyla çalışmanızı gerektirir.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Senaryo 1: Etiketleri web istemcisinden yeniden yazdırma

Dalga etiketlerini aşağıdaki sayfalardan görüntüleyebilir ve yeniden yazdırabilirsiniz. Her sayfanın Eylem Bölmesinde **Sevkiyatlar** sekmesindeki **İlgili bilgiler** grubunda **Dalga etiketleri** 'ni seçin.

- Tüm sevkiyatlar \> Sevkiyat ayrıntıları
- Tüm yükler \> Yük ayrıntıları
- Tüm dalgalar
- Dalga etiketleri
- Dalga etiketi geçmişi

Bir dalga etiketini web istemcisinden yeniden yazdırmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar** 'a gidin.
1. Etiketlerin yeniden yazdıralacağı dalgayı seçin.
1. Eylem Bölmesinde, **Dalga** sekmesindeki **Yazdır** gurubunda **Dalga etiketleri** 'ni seçin.
1. Aşağıdaki adımlardan birini veya her ikisini izleyin:

    - Etiketi yeniden yazdırmak için **Yazıcı adı** alanında yazıcıyı seçin. (Etiketi yeniden yazdırmadan yalnızca dalga etiketi ayrıntılarını güncelleştirmek istiyorsanız bu alanı boş bırakın.)
    - Etiketi güncelleştirmek için, **Dalga etiketi ayrıntılarını güncelleştir** onay kutusunu seçin. (Yalnızca önceki etiketi yeniden yazdırmak istiyorsanız bu onay kutusunu boş bırakın.)

    > [!NOTE]
    > Bir dalga etiketi her yazdırıldığında veya yeniden yazdırıldığında, verileri uygun dalga etiketi düzeniyle dönüştürülür ve tüm yer tutucular gerçek değerlerle değiştirilir. Sonuçta elde edilen dize, dalga etiketi geçmişinde bir kayıt olarak depolanır. **Dalga etiketi ayrıntılarını güncelleştir** onay kutusu temizlenirse, etiket yeniden yazdırıldığında depolanan Zebra Programlama Dili (ZPL) verileri kullanılır. **Dalga etiketi ayrıntılarını güncelleştir** onay kutusu işaretliyse, yeni bir dize oluşturulur. Mevcut dalga etiketleri de yeniden hesaplanır ve fazla etiketler (örneğin, ilgili iş satırları iptal edildiyse veya değiştirilirse) **Hükümsüz kılındı** olarak işaretlenir ve tekrar yazdırılmaz.

1. Seçiminizi onaylamak için **Tamam** 'ı seçin.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Senaryo 2: Etiketleri ambarlama uygulamasından yeniden yazdırma

Bu senaryo genellikle bir etiket rulosu kaybedildiyse veya zarar görürse geçerlidir. Çalışanların tek ve birden çok etiketi yeniden yazdırmasına olanak tanıyacak mobil cihaz menü öğelerinin nasıl ayarlanacağını gösteren bir örnek sağlar. Daha sonra, bu yeni menü öğelerinin mobil cihazda çalışırken nasıl kullanılacağını gösterir.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Mobil cihaz için gerekli menü öğelerini ve menüyü ayarlama

Çalışanların etiketleri mobil cihazdan yeniden yazdırabilmesi için, menü öğelerini bu işlevleri sağlayacak şekilde ayarlamanız ve sonra bu öğeleri ambar uygulama menüsüne eklemeniz gerekir.

#### <a name="create-new-mobile-device-menu-items"></a>Yeni mobil cihaz menü öğeleri oluşturma

Ambarlama uygulamasından etiketleri yeniden yazdırmak için yeni bir menü öğeleri koleksiyonu oluşturmak üzere bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri** 'ne gidin.
1. Menü öğesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Tek bir dalga etiketini yeniden yazdır*
    - **Başlık:** *Tek bir dalga etiketini yeniden yazdır*
    - **Mod:** *Dolaylı*
    - **Faaliyet kodu:** *Tek dalga etiketini yeniden yazdır*

1. İkinci bir menü öğesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Etiketleri yeniden yazdır (Madde)*
    - **Başlık:** *Etiketleri yeniden yazdır (Madde)*
    - **Mod:** *Dolaylı*
    - **Faaliyet kodu:** *Birden fazla dalga etiketini yeniden yazdır*
    - **İş listesigruplandırma filtresini görüntüle:** *Evet*
    - **Sistem gruplandırma alanı:** *ShipmentID*
    - **Sistem gruplandırma etiketi:** *Sevkiyat kodu*
    - **Yazdırma modu:** *Ürün*

1. Eylem Bölmesinde, çalışanların doğru etiket rulosunu belirlemesine yardımcı olacak alanları seçebileceğiniz bir sayfa açmak için **Alan listesi** 'ni seçin.
1. En çok yedi alan gösterebilirsiniz. Kullanılabilir her konumda gösterilen alanı seçmek için aşağı açılan listeleri kullanın. Gerekli olmayan alanları boş bırakın. 

    Aşağıda bir örnek verilmiştir:

    - **Alanı görüntüle:** *LabelItemId*
    - **Alanı görüntüle 2:** *LabelItemName*
    - **Alanı görüntüle 3:** *InventQty*
    - **Alanı görüntüle 4:** *LabelUnitId*

1. Sayfayı kapatın.
1. Üçüncü bir menü öğesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Etiketleri yeniden yazdır (Numaralandırma)*
    - **Başlık:** *Etiketleri yeniden yazdır (Numaralandırma)*
    - **Mod:** *Dolaylı**
    - **Faaliyet kodu:** *Birden fazla dalga etiketini yeniden yazdır*
    - **İş listesigruplandırma filtresini görüntüle:** *Evet*
    - **Sistem gruplandırma alanı:** *ShipmentID*
    - **Sistem gruplandırma etiketi:** *Sevkiyat kodu*
    - **Yazdırma modu:** *Numaralandırma*

1. Eylem bölmesinde, **Alan listesi** 'ni seçin ve sonra çalışanların doğru etiket rulosunu tanımlamasına yardımcı almak için gösterilecek alanları seçmek için aşağı açılır listeleri kullanın (örneğin, *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* , and *NumberOfLabels* ).
1. Sayfayı kapatın.
1. Dördüncü bir menü öğesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Etiketleri yeniden yazdır (sonuncuya göre)*
    - **Başlık:** *Etiketleri yeniden yazdır (sonuncuya göre)*
    - **Mod:** *Dolaylı*
    - **Faaliyet kodu:** *Birden fazla dalga etiketini yeniden yazdır*
    - **İş listesigruplandırma filtresini görüntüle:** *Evet*
    - **Sistem gruplandırma alanı:** *ShipmentID*
    - **Sistem gruplandırma etiketi:** *Sevkiyat kodu*
    - **Yazdırma modu:** *Son iyi dalga etiketi kodu*

1. Eylem bölmesinde, **Alan listesi** 'ni seçin ve sonra çalışanların doğru etiket rulosunu tanımlamasına yardımcı almak için gösterilecek alanları seçmek için aşağı açılır listeleri kullanın (örneğin, *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* , and *NumberOfLabels* ).
1. Sayfayı kapatın.

#### <a name="set-up-the-mobile-device-menu"></a>Mobil cihaz menüsünü ayarlama

Yeni menü öğelerinizi ambarlama uygulaması menüsüne eklemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü** 'ne gidin.
1. Mevcut bir **Çıkış** menüsü seçin.
1. Soldaki listede, yeni oluşturduğunuz yeniden yazdır menü öğelerini bulun ve sağdaki listeye eklemek için sağ ok düğmesini kullanın.
1. Sayfayı kapatın.

### <a name="use-cases"></a>Kullanım örnekleri

Burada sağlanan kullanım örnekleri, ayarladığınız çeşitli mobil cihaz menü öğelerinin çalışanların dalga etiketlerini yeniden yazdırmasına olanak sağlayacak şekilde nasıl kullanılacağını gösteren örnekler verir.

Bu kullanım örneklerini kullanmaya başlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Demo verileri yüklenmiş olmalıdır ve **USMF** tüzel kişiliğini seçmeniz gerekir.
- Dalga etiketi yazdırma yapılandırılmalı ve [Dalga etiketi yazdırmayı yapılandır](../warehousing/configure-wave-label-printing.md) bölümünde açıklandığı gibi bazı etiketler oluşturulmalıdır.

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Kullanım örneği 2.1: Tek bir dalga etiketi çizilmiş ve yeniden yazdırmalı.

1. Ambar uygulamasında ambar *62* 'ye erişimi olan bir kullanıcı olarak oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak *62* ve parola olarak *1* kullanarak oturum açabilirsiniz.)
1. **Giden \> Tek bir dalga etiketini yeniden yazdır** 'ı seçin.
1. Dalga etiketi kodunu girin veya tarayın.
1. Yeniden yazdırma yapılacak yazıcıyı seçin.
1. Eylemi onaylamak için **Tamam** 'ı seçin.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Kullanım örneği 2.2: Aynı maddenin bazı kutu etiketleri zarar görmüş ve yeniden yazdırılmalı. Her etikette bir ürün barkodu bulunur ancak numaralandırma veya SSCC numarası yoktur.

1. Ambar uygulamasında ambar *62* 'ye erişimi olan bir kullanıcı olarak oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak *62* ve parola olarak *1* kullanarak oturum açabilirsiniz.)
1. **Giden \> Etiketleri yeniden yazdır (Madde) gidin**.
1. Sevkiyat kodunu girin veya tarayın.
1. Yeniden yazdırılacak için doğru etiket rulosuna sahip kutucuğu seçin.
1. Doğru satırın seçilmiş olduğunu onaylamak için mevcut bir etiketten ürün barkodunu tarayın.
1. Yeniden yazdırılacak etiket sayısını girin.
1. Yeniden yazdırma yapılacak yazıcıyı seçin.
1. Eylemi onaylamak için **Tamam** 'ı seçin.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Kullanım örneği 2.3: Yazıcıya kağıt sıkıştığı için bazı kutu etiketleri yazdırılmadı. Etiketlerin numaralandırması olduğundan, yeniden yazdırılacak kutu aralığını tanımlayabilirsiniz.

1. Ambar uygulamasında ambar *62* 'ye erişimi olan bir kullanıcı olarak oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak *62* ve parola olarak *1* kullanarak oturum açabilirsiniz.)
1. **Giden \> Etiketleri yeniden yazdır (Numaralandırma) gidin**.
1. Sevkiyat kodunu girin veya tarayın.
1. Yeniden yazdırılacak için doğru etiket rulosuna sahip kutucuğu seçin.
1. Etiketi yeniden yazdıracağınız ilk koliyi girin.
1. Etiketi yeniden yazdıracağınız son koliyi girin. Alternatif olarak, belirtilen ilk koliden sonra tüm koliler için etiketleri yeniden yazdırmak üzere bu alanı boş bırakın.
1. Yeniden yazdırma yapılacak yazıcıyı seçin.
1. Eylemi onaylamak için **Tamam** 'ı seçin.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Kullanım örneği 2.4: Yazıcıya kağıt sıkıştığı için bazı kutu etiketleri yazdırılmadı. Düzgün yazdırılan son etikette barkod olarak olarak yazdırılmış dalga etiketi kodu var.

1. Ambar uygulamasında ambar *62* 'ye erişimi olan bir kullanıcı olarak oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak *62* ve parola olarak *1* kullanarak oturum açabilirsiniz.)
1. **Giden \> Etiketleri yeniden yazdır (sonuncuya göre) gidin**.
1. Sevkiyat kodunu girin veya tarayın.
1. Yeniden yazdırılacak için doğru etiket rulosuna sahip kutucuğu seçin.
1. Düzgün son dalga etiketinin dalga etiketi kodunu girin veya tarayın. Uygulama, sıradaki sonraki etiketi bir etiketin yeniden yazdırılacağı ilk kutu olarak tanımlar.
1. Etiketi yeniden yazdıracağınız son koliyi girin. Alternatif olarak, belirtilen ilk koliden sonra tüm koliler için etiketleri yeniden yazdırmak üzere bu alanı boş bırakın.
1. Yeniden yazdırma yapılacak yazıcıyı seçin.
1. Eylemi onaylamak için **Tamam** 'ı seçin.

## <a name="scenario-3-short-pick-and-reprint"></a>Senaryo 3: Eksik çekme ve yeniden yazdırma

Bu senaryoyu kullanmaya başlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Demo verileri yüklenmiş olmalıdır ve **USMF** tüzel kişiliğini seçmeniz gerekir.
- Dalga etiketi yazdırma yapılandırılmalı ve [Dalga etiketi yazdırmayı yapılandır](../warehousing/configure-wave-label-printing.md) bölümünde açıklandığı gibi bazı etiketler oluşturulmalıdır.

### <a name="set-up-work-exceptions"></a>İş özel durumlarını ayarla

İş özel durumları eksik malzeme çekme davranışını denetler. İş özel durumu ayarlamak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> İş \> İş özel durumları** 'na gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **İş özel durumu kodu:** *Eksik çekme ve yazdırma*
    - **Özel durum türü:** *Eksik çekme*
    - **Dalga etiketlerini yeniden yazdırmayı öner:** *Evet*

### <a name="void-and-reprint-after-a-short-pick"></a>Eksik çekme işleminden sonra hükümsüz kıl ve yeniden yazdır

1. Ambar uygulamasında ambar *62* 'ye erişimi olan bir kullanıcı olarak oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak *62* ve parola olarak *1* kullanarak oturum açabilirsiniz.)
1. Dalga etiketleri ilk kez yazdırıldığında oluşturulan satış siparişi işi için bir iş işleme akışı açın.
1. **Eksik çekme** 'yi seçin.
1. Bu senaryo için oluşturduğunuz iş özel durum kodunu seçin.
1. Doğru özel durumu seçtiyseniz, **Hükümsüz kıl ve yeniden yazdır** onay kutusu kullanılabilir olmalıdır. Bu kutuyu seçin ve onaylayın. Onaylandığında, **Etiket derleme kodu** alanı tarafından tanımlanan etiket rulosu sırası değiştirilen iş satırı miktarına göre yeniden hesaplanır. Belirtilen yazıcıda yeniden yazdırılır.
