--- 
title: "RFQ kullanan bir talep oluşturma"
description: "Bu kılavuz, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini gösterir."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 14eed7982041b7af7dad5453b10f07f063ba1855
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>RFQ kullanan bir talep oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini gösterir. Bu kılavuzda gösterilen örnek USMF demo verileri şirketinde kullanılabilir ve tüm adımları tamamlamak için bir Yönetici olarak oturum açmanız gerekir. Bu kılavuzdaki görevler genellikle tedarik profesyonelleri tarafından yapılır.


## <a name="create-a-requisition"></a>Talep oluşturun
1. Tedarik ve kaynak Hizmeti'nden > Satınalma talepleri > Satınalma talepleri benim tarafından hazırlandı'ya git.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Talep edilen tarih alanında, bir tarih girin.
5. Muhasebe tarihi alanında bir tarih girin.
6. Tamam'ı tıklatın.
7. Neden alanında bir değer girin veya bir değer seçin.
8. Satır ekle'ye tıklayın.
9. Tedarik kategorisi alanında ağaç içinde bir kategori seçin ve Tamam'a tıklayın.
10. Ürün adı alanına bir değer girin.
11. Miktar alanına bir sayı girin.
12. Birim alanına bir değer girin veya buradan bir değer seçin.
13. Kaydet'e tıklayın.
14. İletişim kutusu formunu açmak için İş akışı'na tıklayın.
15. Gönder'i tıklatın.
16. Sayfayı kapatın.
17. Gönder'i tıklatın.

## <a name="reassign-a-workflow-task"></a>İş akışı görevini yeniden atayın
    * Sonraki görev satıcılardan ürün için teklifleri almak için bir RFQ oluşturmaktır. USMF demo verilerinde talep iş akışı, bir satıcı seçilmediğinde veya bir satır için birim fiyat 0 olduğunda belirli bir çalışana bir RFQ oluşturması için bir görevin atandığı bir kural ile ayarlanmıştır. Bu kılavuz ile devam etmek için bu görevi başka bir kullanıcıya (kendinize) yeniden atamanız gerekir. Bunu yalnızca bir Yönetici olarak oturum açtıysanız yapabilirsiniz.  
1. İletişim kutusu formunu açmak için İş akışı'na tıklayın.
2. Geçmişi görüntüle'ye tıklayın.
3. Sayfayı yenileyin.
4. İzleme ayrıntıları bölümünü genişletin.
5. Ağaç içinde, "Satır maddesi iş akışı etkinleştirildi" ile başlayan satırı seçin.
6. İş akış ayrıntılarını görüntüle'ye tıklayın.
7. İş öğeleri bölümünü genişletin.
8. Yeniden Ata'ya tıklayın.
9. Kullanıcı alanında Yönetici'yi seçin.
10. Yeniden Ata'ya tıklayın.
11. Sayfayı kapatın.
12. Sayfayı kapatın.

## <a name="create-an-rfq"></a>RFQ oluşturun
1. Sayfayı yenileyin.
2. Teklif talebi'ne tıklayın.
3. Satın alma tüzel kişiliği alanında USMF'yi seçin.
    * Talep satırında bulunan aynı yasal varlığı seçmelisiniz.  
4. Listede, seçili satırı işaretleyin.
    * Satınalma talebinde birden fazla satırınız varsa RFQ'ya eklemek istediğiniz tüm satırları seçin.  
5. Tamam'a tıklayın.
6. Sayfayı yenileyin.
7. Bilgi kutusunu açın ve ardından İlgili belgeler bölümünü genişletin.
    * Bilgi kutusu zaten açık olabilir. Satırlar/Başlık geçiş düğmelerinin sağında, üzerinde bir ok olan simgeyi arayın. Ok sağı gösteriyorsa bilgi kutusu zaten açıktır. Ok solu gösteriyorsa bilgi kutusunu açmak için oka tıklayın.  
8. Yeni oluşturulan RFQ'yu açmak için Teklif talebi alanındaki bağlantıya tıklayın.
9. Başlık'a tıklayın.
10. Ekle öğesini tıklatın.
11. Satıcı hesabı alanında bir değer girin veya bir değer seçin.
12. Ekle öğesini tıklatın.
13. Satıcı hesabı alanında bir değer girin veya bir değer seçin.
14. Gönder'e tıklayın.
15. Tamam'a tıklayın.
16. Yanıt gir düğmesini tıklayın.
17. Eylem Bölmesinde, Yanıtla öğesine tıklayın.
18. Verileri yanıta kopyala düğmesini tıklayın.
    * Bu, RFQ'dan yanıta miktar ve tarihler gibi verileri kopyalar.  
19. Birim fiyatı alanına bir sayı girin.
    * Bu, satıcıdan aldığınız fiyattır. Ayrıca satıcıdan ek bilgiler girmek de isteyebilirsiniz.  
20. Kabul et düğmesini tıklatın.
21. Tamam'a tıklayın.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Satıcı ve fiyatın talebe aktarılmış olduğunu doğrulayın
1. Sayfayı kapatın.
2. Satırlar seçeneğine tıklayın.
3. İlgili bilgiler'e tıklayın.
4. Satınalma talebi'ne tıklayın.
5. RFQ'ya transfer edilen satırı seçin.
    * Fiyatın ve satıcının talebe kopyalandığını doğrulayın.  
6. İletişim kutusu formunu açmak için İş akışı'na tıklayın.
7. Tamamla öğesine tıklayın.
8. Sayfayı kapatın.
9. Tamamla öğesine tıklayın.

