---
title: "Şirketlerarası faturalama"
description: "Bu makalede, Microsoft Dynamics 365 for Finance and Operations'ta projeler için şirketlerarası faturalama hakkında bilgiler ve örnekler verilir."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 7cd19340c913fcda3fb537162dfbae52b5c8e922
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="intercompany-invoicing"></a>Şirketlerarası faturalama

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Finance and Operations'ta projeler için şirketlerarası faturalama hakkında bilgiler ve örnekler verilir.

Kuruluşunuzda projeler için ürünler ve hizmetleri birbirlerine aktaran birden çok bölüm, yan kuruluşlar ve diğer tüzel kişilikler olabilir. Hizmet veya ürün sağlayan tüzel kişiliğe *ödünç veren tüzel kişilik* ve servis veya ürün alan tüzel kişiliğe ise *ödünç alan tüzel kişilik* adı verilir. 

Aşağıdaki çizim iki tüzel kişilik olan SI FR (ödünç alan tüzel kişilik) ve SI USA (ödünç veren tüzel kişilik)'nın müşteri A için bir proje teslim etmek amacıyla kaynakları paylaştıkları tipik bir senaryoyu gösterir. 

[![Şirketlerarası faturalama örneği](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Amaç maliyet kontrolü, gelir kabulü, vergileri yapmak ve şirketlerarası proje hareketleri için fiyatı daha esnek ve güçlü aktarmaktır. Buna ek olarak aşağıdaki yetenekler sağlanır:

-   Bir ödünç veren tüzel kişilikteki şirketlerarası zaman çizelgeleri, giderler ve satıcı faturalarını kullanarak bir ödünç alan tüzel kişilikteki projeye göre müşteri faturaları oluşturun.
-   Vergi hesaplamaları ve dolaylı maliyetleri destekleyin.
-   Ödünç veren tüzel kişilikteki gelir kabulünü ve ödünç alan tüzel kişiliğin maliyeti tanıması gereken zamanı erteleyin.
-   Ödünç veren tüzel kişilikte işlem (WIP) gelirine işi tahakkuk ettirin.
-   Çeşitli fiyatlama modellerini temel alabilen transfer fiyatlarını ayarlayın. Burada bazı örnekler verilmiştir:
    -   **Miktar**: **Fiyatlandırma** alanına girdiğiniz tutar miktar veya birim başına gerçek maliyettir.
    -   **Masraf tutarı**: Hareket başına fiyat/maliyet artı **Fiyatlama** alanına girdiğiniz masraf tutarıdır.
    -   **Masraflar yüzdesi**: Transfer fiyatı hareket başına fiyat/maliyetin **Fiyatlama** alanına girdiğiniz masraflar yüzdesi ile çarpımıdır.
    -   **Satış fiyatı yüzdesi**: Ödünç veren tüzel kişiliğe aktarılan satış fiyatı yüzdesidir.
    -   **Satış fiyatının altındaki tutar**: Ödünç veren tüzel kişiliğe aktarmadan önce ödünç alan tüzel kişiliğin satış fiyatlarından geri tuttuğu tutardır.
    -   **Katkı oranı**: **Fiyatlandırma** alanına girdiğiniz sayı katkı oranı olup satış fiyatının yüzdesi olarak ifade edilir.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Örnek 1: Şirketlerarası faturalama için parametreleri ayarlayın
Bu örnekte USSI ödünç veren tüzel kişiliktir ve kaynakları son müşteri ile sözleşmesi olan ödünç alan tüzel kişilik FRSI'ye karşılık zaman raporlar. USSI çalışanlarının raporladığı saatler ve masraflar FRSI'nın oluşturduğu proje faturasına dahil edilebilir. Ayrıca yan şirketlere paylaşılan satıcı hizmetlerini sağladığında ödünç veren tüzel kişilikten gelen üçüncü bir hareket kaynağı vardır ve sonra bu maliyetler üzerinden bu yan şirketlerdeki projelere geçer. Tüm eşleşen fatura belgeleri ve vergi hesaplamaları Finance and Operations tarafından tamamlanır. 

Bu örnek için FRSI, USSI tüzel kişiliğinde bir müşteri olmalı ve USSI, FRSI tüzel kişiliğinde bir satıcı olmalıdır. Daha sonra iki tüzel kişilik arasında şirketlerarası bir ilişki kurabilirsiniz. Aşağıdaki prosedür her iki tüzel kişiliğin de şirketlerarası faturalamaya katılabilmesi için gereken parametrelerin nasıl ayarlanacağını gösterir.

1.  USSI tüzel kişiliğinde FRSI'yı müşteri olarak ve FRSI tüzel kişiliğinde USSI'yı satıcı olarak ayarlayın. Bu görevin gerektirdiği adımlar için üç giriş noktası vardır.
    | Adım | Giriş noktası                                                                       | Açıklama   |
    |------|-----------------------------------------------------------------------------------|------------------|
    | A:    | USSI'da **Alacak hesapları** &gt; **Müşteriler** &gt; **Tüm müşteriler**'e tıklayın. | FRSI için yeni bir müşteri kaydı oluşturun ve müşteri grubunu seçin.                                                                                  |
    | B:    | FRSI'da **Borç hesapları** &gt; **Satıcılar** &gt; **Tüm satıcılar**'a tıklayın.        | USSI için yeni bir satıcı kaydı oluşturun ve satıcı grubunu seçin.                                                                                    |
    | A    | FRSI'da yeni oluşturduğunuz satıcı kaydını açın.                            | Eylem Bölmesinde, **Genel** sekmesindeki **Ayarla** gurubunda **Şirketlerarası**'na tıklayın. **Şirketlerarası** sayfasındaki **Ticari ilişki** sekmesinde **Etkin** kaydırma çubuğunu **Evet** konumuna getirin. **Müşteri şirketi** alanında adım A'da oluşturduğunuz müşteri kaydını seçin. |

2.  **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Proje yönetimi muhasebe parametreleri** üzerine tıklayın ve sonra **Şirketlerarası** sekmesine tıklayın. Parametreleri ayarlama şekliniz ödünç veren tüzel kişilik veya ödünç alan tüzel kişilik olmanıza göre değişir.
    -   Ödünç alan tüzel kişilikseniz otomatik olarak oluşturulan ve satıcı faturalarını eşleştirmek için kullanılması gereken tedarik kategorisini seçin.
    -   Ödünç alan tüzel kişilikseniz her bir ödünç alan tüzel kişilik için her bir hareket türüne ait varsayılan proje kategorisini seçin. Şirketlerarası hareketlerde faturalandırılmış kategori yalnızca ödünç alan tüzel kişilikte varken proje kategorileri vergi yapılandırması için kullanılır. Şirketlerarası hareketler için geliri tahakkuk ettirmeyi seçebilirsiniz. Bu tahakkuk hareketler nakledildiğinde yapılır ve sonra şirketlerarası fatura nakledildiğinde tersine çevrilir.

3.  **Proje yönetimi ve muhasebe** &gt; **Ayar** &gt; **Fiyatlar** &gt; **Transfer fiyatı**'na tıklayın.
4.  Para birimini, hareket türünü ve transfer fiyatı modelini seçin. Faturada kullanılan para birimi ödünç veren tüzel kişilikte ödünç alan tüzel kişilik için müşteri kaydında yapılandırılan para birimidir. Para birimi transfer fiyat tablosundaki girişleri eşleştirmek için kullanılır.
5.  **Genel muhasebe** &gt; **Deftere nakil kurulumu** &gt; **Şirketlerarası muhasebe**'ye tıklayın ve USSI ve FRSI için bir ilişki ayarlayın.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Örnek 2: Şirketlerarası zaman çizelgesi oluşturun ve nakledin
USSI, ödünç veren tüzel kişilik FRSI ödünç alan şirketten gelen bir proje için zaman çizelgesi oluşturmalı ve nakletmelidir. Bu görevin gerektirdiği adımlar için iki giriş noktası vardır.

| Adım | Giriş noktası                                                                       | Açıklama                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | **Proje yönetimi ve muhasebe** &gt; **Zaman çizelgeleri** &gt; **Tüm zaman çizelgeleri** | Yeni bir zaman çizelgesi oluştur. Zaman çizelgesi satırı üzerinde bulunan **Tüzel kişilik** alanında **FRSI**'yı seçin. **Proje kimliği** alanında, FRSI'daki projeyi seçin. Haftanın her günü için saatleri girin. |
| B:    | **Zaman Çizelgesi** sayfası                                                                | İş akışını çalıştırdıktan sonra zaman çizelgesini nakledin ve fiş numarasını not alın.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Örnek 3: Şirketlerarası satıcı faturası oluşturun ve nakledin
USSI, ödünç veren tüzel kişilik FRSI ödünç alan şirketten gelen bir proje için şirketlerarası satıcı faturası oluşturmalı ve nakletmelidir. Bu satıcı faturası dış kaynak işgücünü ve USSI tarafından ödenen satıcıların gerçekleştirdiği masrafı gösterir. Bu görevin gerektirdiği adımlar için iki giriş noktası vardır.

| Aşama | Giriş noktası                                                                                      | Açıklama                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | **Borç hesapları** &gt; **Faturalar** &gt; **Satıcı faturalarını aç** &gt; **Yeni satıcı faturası** | Yeni bir satıcı faturası oluşturun ve FRSI projesi adına tedarik edilen hizmetleri girin.                                                                                                                                                                                  |
| B:    | **Satıcı faturası** sayfası                                                                      | FRSI adına dış kaynak hizmetlerini gösteren satırlar girin. **Satır ayrıntıları** Hızlı Sekmesindeki, fatura için **Proje** sekmesinde **Proje şirketi** alanına **FRSI**'yı girin. Proje ve ilgili bilgileri girin. Sonra satıcı faturasını nakledin. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Örnek 4: Şirketlerarası fatura oluşturun ve nakledin
USSI, ödünç veren tüzel kişilik oluşturulmalı ve şirketlerarası fatura nakledilmelidir. Bu görevin gerektirdiği adımlar için iki giriş noktası vardır.

| Adım | Giriş noktası                                                                                             | Açıklama                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturası**  | **Şirketlerarası fatura oluştur** sayfasını açmak için **Yeni** 'ye tıklayın.                                                                                  |
| B:    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları** | **Şirketlerarası fatura oluştur** sayfasında tüzel kişiliği girin, dahil edilecek hareketi belirtin ve sonra **Ara**'ya tıklayın. |
| A    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları** | Faturayla ilgili hareketleri seçin veya listedeki tüm hareketleri faturalandırmak için **Tümünü Seç**'e tıklayın ve sonra **Tamam**'a tıklayın.                  |
| B    | **Şirketlerarası fatura** sayfası                                                                       | Şirketlerarası müşteri fatura teklifi gösterilir.                                                                                             |
| E:    | **Şirketlerarası fatura** sayfası                                                                       | **Naklet**'e tıklayın.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Örnek 5: Satıcı faturasını nakledin ve müşteriye faturalandırın
USSI ödünç veren tüzel kişiliği şirketlerarası müşteri faturasını naklettiğinde, eşleşen beklemedeki satıcı faturası FRSI ödünç alan tüzel kişilikte oluşturulur. Bu satıcı faturası nakledildiğinde FRSI da USSI'nın girildiği saatler için proje müşterisine faturalandırma yapar. Bu görevin gerektirdiği adımlar için üç giriş noktası vardır.

| Aşama | Giriş noktası                                                                                        | Açıklama                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A:    | **Borç hesapları** &gt; **Faturalar** &gt; **Bekleyen satıcı faturaları**                            | Zaman çizelgesi değerlerinin dahil edildiğini doğrulamak için faturayı gözden geçirin ve sonra satıcı faturasını nakledin.                  |
| B:    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Proje fatura teklifleri** | Proje için yeni bir proje faturası oluşturun ve nakledilen saat hareketlerinin görüntülendiğini doğrulayın.            |
| A    | **Proje faturası** sayfası                                                                       | Proje faturasını seçin ve ardından maliyet ve satış tutarını gözden geçirmek için **Ayrıntıları görüntüle**'ye tıklayın. Sonra faturayı nakledin. |


Daha fazla bilgi için bkz [Şirketlerarası proje faturalaması yapılandırma](tasks/configure-intercompany-project-invoicing.md).



