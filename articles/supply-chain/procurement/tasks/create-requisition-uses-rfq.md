---
title: RFQ kullanan bir talep oluşturma
description: Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 65c6c7b718b3538ebd0096cd173c933b9d750da1102b0c32d73200f4428026a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776350"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>RFQ kullanan bir talep oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar. Bu kılavuzda gösterilen örnek USMF demo verileri şirketinde kullanılabilir ve tüm adımları tamamlamak için bir Yönetici olarak oturum açmanız gerekir. Bu kılavuzdaki görevler genellikle tedarik profesyonelleri tarafından yapılır.


## <a name="create-a-requisition"></a>Talep oluşturun
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tarafımdan hazırlanan satınalma talepleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir değer yazın.
4. **Talep edilen tarih** alanına, bir tarih girin.
5. **Muhasebe tarihi** alanına bir tarih girin.
6. **Tamam**'ı seçin.
7. **Neden** alanında bir değer girin veya bir değer seçin.
8. **Satır ekle**'yi seçin.
9. **Tedarik kategorisi** alanında ağaç içinde bir kategori seçin ve **Tamam**'a tıklayın.
10. **Ürün adı** alanına bir değer yazın.
11. **Miktar** alanına bir sayı girin.
12. **Birim** alanına bir değer girin veya buradan bir değer seçin.
13. **Kaydet**'i seçin.
14. Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.
15. **Gönder**'i seçin.
16. Sayfayı kapatın.
17. **Gönder**'i seçin.

## <a name="reassign-a-workflow-task"></a>İş akışı görevini yeniden atayın
Sonraki görev satıcılardan ürün için teklifleri almak için bir RFQ oluşturmaktır. USMF demo verilerinde talep iş akışı, bir satıcı seçilmediğinde veya bir satır için birim fiyat 0 olduğunda belirli bir çalışana bir RFQ oluşturması için bir görevin atandığı bir kural ile ayarlanmıştır. Bu kılavuz ile devam etmek için bu görevi başka bir kullanıcıya (kendinize) yeniden atamanız gerekir. Bunu yalnızca bir Yönetici olarak oturum açtıysanız yapabilirsiniz.  

1. Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.
2. **Geçmişi görüntüle**'yi seçin.
3. Sayfayı yenileyin.
4. **İzleme ayrıntıları**  bölümünü genişletin.
5. Ağaçta, "Satır iş akışı etkinleştirildi" ile başlayan satırı seçin.
6. **İş akış ayrıntılarını görüntüle**'yi seçin.
7. **İş öğeleri**  bölümünü genişletin.
8. **Yeniden ata**'yı seçin.
9. **Kullanıcı** alanında **Yönetici**'yi seçin.
10. **Yeniden ata**'yı seçin.
11. İki sayfayı da kapatın.

## <a name="create-an-rfq"></a>RFQ oluşturun

1. Sayfayı yenileyin.
2. **Teklif talebi**'ni seçin.
3. **Satın alma tüzel kişiliği** alanında **USMF**'yi seçin. Talep satırında bulunan aynı yasal varlığı seçmelisiniz.  
4. Listede, seçili satırı işaretleyin. Satınalma talebinde birden fazla satırınız varsa RFQ'ya eklemek istediğiniz tüm satırları seçin.  
5. **Tamam**'ı seçin.
6. Sayfayı yenileyin.
7. Bilgi kutusunun açık olduğundan emin olun ve **İlgili belgeler** bölümünü genişletin.
8. Yeni oluşturulan RFQ'yu açmak için **Teklif talebi** alanındaki bağlantıyı seçin.
9. **Başlık** öğesini seçin.
10. **Ekle**'yi seçin.
11. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.
12. **Ekle**'yi seçin.
13. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.
14. **Gönder**'i seçin.
15. **Tamam**'ı seçin.
16. **Yanıt gir**'i seçin.
17. Eylem Bölmesinde, **Yanıtla**'yı seçin.
18. **Verileri yanıta kopyala**'yı seçin. Bu, RFQ'dan yanıta miktar ve tarihler gibi verileri kopyalar.  
19. **Birim fiyatı** alanına bir sayı girin. Bu, satıcıdan aldığınız fiyattır. Ayrıca satıcıdan ek bilgiler girmek de isteyebilirsiniz.  
20. **Kabul et**'i seçin.
21. **Tamam**'ı seçin.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Satıcı ve fiyatın talebe aktarılmış olduğunu doğrulayın
1. Sayfayı kapatın.
2. **Satırlar**'ı seçin.
3. **İlgili bilgiler**'i seçin.
4. **Satınalma talebi**'ni seçin.
5. RFQ'ya transfer edilen satırı seçin. Fiyatın ve satıcının talebe kopyalandığını doğrulayın.  
6. Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.
7. Tamamlandı'yı seçin.
8. Sayfayı seçin.
9. Tamamlandı'yı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]