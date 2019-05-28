---
title: 'Döngü sayımı tanımlama '
description: Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571718"
---
# <a name="define-cycle-counting"></a>Döngü sayımı tanımlama  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir. Bu görev kaydı; varsayılan sayım işi önceliğinin ayarlanmasını, hem çekme hem de sayım süreçlerini işlemek için mobil cihaz menü öğesinin etkinleştirilmesini, bir konum boşaldığında sayım eşiği tetikleyicisinin etkinleştirilmesini ve belirli bir ambar içindeki belirli bir öğe için döngü sayımı planının etkinleştirilmesini kapsar. Bu görevler genellikle bir ambar yöneticisi tarafından yapılır. Bu yordamı demo verileri şirketi USMF veya kendi verilerinizi kullanarak yerine getirebilirsiniz.


## <a name="set-the-priority-of-counting-work"></a>Sayım çalışma önceliğini ayarlama
1. Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.
2. Döngü sayımı sekmesini tıklatın.
3. Varsayılan döngü sayısı iş önceliği alanına bir sayı girin.
    * Bu adım, ambardaki diğer iş türlerine kıyasla döngü sayımı işinin önceliğini değiştirir. Diğer iş türlerinden daha düşük bir sayı girerek, döngü sayımı işinin önceliğini artırırsınız.  
4. Kaydet'e tıklayın.
5. Sayfayı kapatın.

## <a name="enable-the-mobile-device"></a>Mobil cihazı etkinleştirin
1. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Menü öğesi adı alanına bir değer girin.
4. Başlık alanına bir değer yazın.
5. Mod alanında, 'İş' seçin.
6. Mevcut işin kullanılması seçeneğinde Evet'i işaretleyin.
    * Bu seçeneği Evet olarak ayarladığınızda, sistem, mobil aygıt menü öğesi kullanıldığında var olan işleri arar.  
7. Yöneten alanında Sistem'i seçin.
    * "Sistem tarafından yönlendirilen" seçildiğinde, ambar çalışanı iş sınıflarında tanımlanan açık işe yönlendirilir. (Sırada bu iş sınıflarını oluşturacağız.)  
8. İş sınıfları bölümünü genişletin veya daraltın.
    * Daha sonra bu mobil aygıt menü öğesi ile kullanılacak iki iş sınıfı oluşturacağız. Menü öğesi kullanıldığında, bu iş sınıfları sıraya konulacaktır ve en yüksek önceliğe sahip işin kullanıcıya gösterilecektir.  
9. Yeni'ye tıklayın.
10. İş sınıfı numarası alanına bir değer girin veya buradan bir değer seçin.
11. Yeni'ye tıklayın.
12. İş sınıfı numarası alanına bir değer girin veya buradan bir değer seçin.
13. Kaydet'e tıklayın.
14. Sayfayı kapatın.
15. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğesine gidin.
16. Listede, istenen kaydı bulun ve seçin.
17. Ağaçta, 'oluşturmuş olduğunuz menü öğesini seçin'.
18. Düzenle öğesine tıklayın.
19. Menüye menü öğesi eklemek için oku tıklatın.
20. Kaydet'e tıklayın.

## <a name="create-a-counting-threshold"></a>Bir sayım eşiği yaratın
1. Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı eşikleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Döngü sayımı eşiği numarası alanına bir değer yazın.
4. Döngü sayımını hemen işleme seçeneğinde Evet'i seçin.
5. Açıklama alanına bir değer girin.
6. Kaydet'i tıklatın.
7. Konumları Seç'i tıklatın.
8. Listede, seçili satırı işaretleyin.
9. Ölçütler alanından bir değer seçin.
10. Tamam'a tıklayın.
11. Sayfayı kapatın.

## <a name="create-a-cycle-count-plan"></a>Bir döngü sayım planı yaratın
1. Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı planları öğesine gidin.
2. Yeni'ye tıklayın.
3. Döngü sayımı planı numarası alanına bir değer yazın.
4. Tanım alanına bir değer girin.
5. Maksimum döngü sayımı miktarı alanına bir sayı girin.
6. Kaydet'i tıklatın.
7. Konumları Seç'i tıklatın.
8. Listede, seçili satırı işaretleyin.
9. Ölçütler alanından bir değer seçin.
10. Tamam'a tıklayın.
11. Döngü sayımları arasındaki günler alanına bir sayı girin.
    * Örneğin, döngü sayımı alanında gün olarak belirtilen değer 5 olarak ayarlanmışsa, her beş günde oluşturulur. Ancak, döngü sayımı işi üçüncü günde işleniyorsa, bir sonraki döngü sayımı işi son döngü sayımı işlendikten beş gün sonra, 8. gün içinde oluşturulur.  
12. Kaydet'e tıklayın.
13. Yeni'ye tıklayın.
14. Sıra numarası alanına bir numara girin.
    * Sıralama en küçük sayıdan en büyük sayıyadır. Değer 0'dan (sıfır) fazla olmalıdır.  
15. Listede, seçili satırı işaretleyin.
16. Açıklama alanına bir değer girin.
17. Kaydet'i tıklatın.
18. Ürün sorgusu tanımla'ya tıklayın.
19. Listede, seçili satırı işaretleyin.
20. Ölçütler alanında bir değer girin veya seçin.
21. Tamam'a tıklayın.
22. Sayfayı kapatın.

