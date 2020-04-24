---
title: Teklif talebi oluşturma
description: Bu prosedür, bir satın alma teklifinin nasıl oluşturulacağını gösterir.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c13ed20ec86108bcb9edc0d20d53ff98732b9d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204758"
---
# <a name="create-a-request-for-quotation"></a>Teklif talebi oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür, bir satın alma teklifinin nasıl oluşturulacağını gösterir. Bu işlem tipik olarak bir satın alma temsilcisi tarafından gerçekleştirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce talep türlerini ayarlamış olmanız gerekir. Bu işlemi tamamladıktan ve bir RFQ oluşturduktan ve gönderdikten sonra her bir satıcı için yanıtlar girebilir, bunları karşılaştırabilir ve işi verebilirsiniz.


## <a name="prepare-a-new-rfq"></a>Yeni bir RFQ hazırlama
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri**'ne gidin.
2. **Yeni**'ye tıklayın.
    Şu satın alma türleri kullanılabilir: Satın alma emri (varsayılan): ürün satın alınması teklifini veya ödeme karşılığında ürünlerin satılması teklifinin kabul edildiğini onaylayan belgedir. Satın alma talebi: doğudan bir satın alma talebinden bir RFQ oluşturduğunuzda bu tür otomatik olarak seçilir. Bu seçeneği el ile seçerseniz bir hata alırsınız. Satın alma sözleşmesi: bir üründen belirli bir zaman aralığında belirli bir miktarda veya değerde satın alınması için yapılan sözleşmedir. Bu seçeneği belirlerseniz, satın alma sözleşmesi için geçerli olacak tarih aralığını seçmeniz gerekir.  
3. **Belge başlığı** alanına bir değer girin.
4. **Talep türü** alanına bir değer girin veya buradan bir değer seçin.
    + Talep türüyle bir puanlama yöntemi ilişkilendirilmişse bu, oluşturmakta olduğunuz RFQ için varsayılan puanlama yöntemi olacaktır. Puanlama yönteminin daha sonra değiştirilmesi mümkündür.  
    + **Teslimat tarihi** alanına bir tarih girin.  
    + Maddeleri almak istediğiniz son tarihi seçin.  
    + **Bitiş tarihi ve saati** alanına bir tarih ve saat girin.  
    + Satıcıların RFQ'ya yanıt vermesi gereken son tarihi ve saati belirtin.  
5. **Ambar alanı**'nda bir değer girin veya bir değer seçin. Teslimat adresi varsayılan olarak ambar adresidir.  
6. **Tamam**'a tıklayın.

## <a name="add-lines"></a>Satır ekle

RFQ'nuz hakkında temel bilgileri belirledikten sonra satıcıların teklif vermelerini istediğiniz malları veya hizmetleri belirlersiniz. Madde, varsayılan olarak satır tipindedir.

1. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin. USMF kullanıyorsanız, T0020'yi seçebilirsiniz.  
2. **Miktar** alanına bir sayı girin.
3. **Satır ekle**'ye tıklayın.
4. **Satır türü** alanından 'Kategori' seçin. Stokta olmayan mallar veya hizmetlere yönelik RFQ'lar oluşturmak için Kategori satır türünü kullanabilirsiniz. Daha sonra, bir satın alma kategorileri hiyerarşisinden malların veya hizmetlerin türünü seçmeniz gerekir.  
5. **Satın alma kategorisi** alanına bir değer girin veya buradan bir değer seçin.
6. **Ürün adı** alanına bir değer yazın.
7. **Miktar** alanına bir sayı girin.
8. **Birim** alanına bir değer girin veya buradan bir değer seçin.

## <a name="add-vendors"></a>Satıcı ekle
1. Satır görünümünü Başlık görünümü olarak değiştirmek için **Başlık**'a tıklayın. 
2. **Satıcı** bölümünü genişletin.
3. **Satıcıları otomatik olarak ekle** düğmesini tıklayın. Talep edilen maddelerin satın alma kategorisine bağlı olarak RFQ'ya satıcıları otomatik olarak ekleyebilirsiniz. Satırlara dahil olan kategoriler için onaylanmış satıcılar bulunmuyorsa satıcıları el ile ekleyebilirsiniz.  
4. **Ekle** öğesine tıklayın.
5. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.
6. **Ekle** öğesine tıklayın.
7. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin. Bir satıcıyı seçtiğinizde durumu Oluşturuldu olarak değiştirilir. Bu da satıcı bilgilerinin RFQ'ya kaydedildiği, ancak RFQ'nun satıcıya göndermediğiniz anlamına gelir. Satıcı durumundan bağımsız olarak bir satıcıyı bir RFQ'ya ekleyebilirsiniz.  

## <a name="send-the-rfq-to-vendors"></a>RFQ'yu satıcılara gönderme
1. **Eylem bölmesi**'nde, **Gönder**'e tıklayın. Teklif talebi gönderiliyor sayfasında, listedeki satıcıların RFQ almasını istediğiniz satıcılarla aynı olduğunu kontrol edin.  
2. **Yazdır**'ı tıklatın. Bu iletişim kutusu RFQ'yu yazdırmanıza olanak sağlar. Bir yanıt sayfasını yazdırmayı seçerseniz, bu işlemin içeriği Satın Alma ve Kaynak Kullanımı parametreleri altında tanımlanır. Yanıt sayfalarının nasıl yazdırılacağını seçmek için Yazdırma iletişim kutusunu açtıktan sonra Gelişmiş yazdırma seçeneklerini tıklayın. Oluşturuldu veya Gönderildiği durumuna sahip satırlar içeren her bir satıcı için bir RFQ yazdırılır. İptal edilmiş satırlar ve kaydedilmiş yanıtların yer aldığı satırlar yazdırılmayacaktır.   
3. **İptal**'e tıklayın
4. **Tamam**'a tıklayın.
5. Sayfayı kapatın.
6. Sayfayı kapatın.

## <a name="view-the-rfq-journal"></a>RFQ günlüğünü görüntüleme
1. **Tedarik ve kaynak atama > Teklif talepleri > Teklif talepleri takibi > Teklif talebi günlükleri** öğesine gidin.
2. **Önizleme/Yazdır** düğmesine tıklayın.
3. **Orijinal önizleme**'ye tıklayın.
4. Sayfayı kapatın.
5. Sayfayı kapatın.

