---
title: 'Döngü sayımı tanımlama '
description: Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1424bc4c4ff0f8528d6577e80324082cb2ec7f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977175"
---
# <a name="define-cycle-counting"></a>Döngü sayımı tanımlama  

[!include [banner](../../includes/banner.md)]

Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir. Bu görev kaydı; varsayılan sayım işi önceliğinin ayarlanmasını, hem çekme hem de sayım süreçlerini işlemek için mobil cihaz menü öğesinin etkinleştirilmesini, bir konum boşaldığında sayım eşiği tetikleyicisinin etkinleştirilmesini ve belirli bir ambar içindeki belirli bir öğe için döngü sayımı planının etkinleştirilmesini kapsar. Bu görevler genellikle bir ambar yöneticisi tarafından yapılır. Bu yordamı demo verileri şirketi USMF veya kendi verilerinizi kullanarak yerine getirebilirsiniz.


## <a name="set-the-priority-of-counting-work"></a>Sayım çalışma önceliğini ayarlama
1. **Gezinti bölmesinde**, **Modüller > Ambar yönetimi > Kurulum > Ambar > Yönetim parametrelerine**'ne gidin.
2. **Döngü sayımı** sekmesini tıklatın.
3. **Varsayılan döngü sayısı iş önceliği** alanına bir sayı girin. Bu adım, ambardaki diğer iş türlerine kıyasla döngü sayımı işinin önceliğini değiştirir. Diğer iş türlerinden daha düşük bir sayı girerek, döngü sayımı işinin önceliğini artırırsınız.  
4. **Kaydet**'e tıklayın.
5. Sayfayı kapatın.

## <a name="enable-the-mobile-device"></a>Mobil cihazı etkinleştirin
1. **Gezinti bölmesinde**, **Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. **Menü öğesi adı** alanına bir değer girin.
4. **Başlık** alanına bir değer yazın.
5. **Mod** alanında, 'İş' seçin.
6. **Mevcut işin kullanılması** seçeneğinde Evet'i işaretleyin. Bu seçeneği Evet olarak ayarladığınızda, sistem, mobil aygıt menü öğesi kullanıldığında var olan işleri arar.  
7. **Yöneten** alanında 'Sistem tarafından yönetilen'i seçin. "Sistem tarafından yönlendirilen" seçildiğinde, ambar çalışanı iş sınıflarında tanımlanan açık işe yönlendirilir. (Sırada bu iş sınıflarını oluşturacağız.)  
8. **İş sınıfları** hızlı sekmesini genişletin. Daha sonra bu mobil aygıt menü öğesi ile kullanılacak iki iş sınıfı oluşturacağız. Menü öğesi kullanıldığında, bu iş sınıfları sıraya konulacaktır ve en yüksek önceliğe sahip işin kullanıcıya gösterilecektir.  
9. **Yeni**'ye tıklayın.
10. **İş sınıfı numarası** alanına bir değer girin veya buradan bir değer seçin.
11. **Yeni**'ye tıklayın.
12. **İş sınıfı numarası** alanına bir değer girin veya buradan bir değer seçin.
13. **Eylem Bölmesi**'nde, **Kaydet** öğesine tıklayın.
14. Sayfayı kapatın.
15. **Gezinti bölmesinde**, **Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.
16. Listede, istenen kaydı bulun ve seçin.
17. Ağaçta, 'oluşturmuş olduğunuz menü öğesini seçin'.
18. **Düzenle**'yi tıklatın.
19. Menüye menü öğesi eklemek için oku tıklatın.
20. **Kaydet**'e tıklayın.

## <a name="create-a-counting-threshold"></a>Bir sayım eşiği yaratın
1. **Gezinti bölmesinde**, **Modüller > ambar yönetimi > Kurulum > döngü sayımı > döngü sayısı eşiklerine** gidin.
2. **Yeni**'ye tıklayın.
3. **Döngü sayımı eşiği numarası** alanına bir değer yazın.
4. **Döngü sayımını hemen işleme** seçeneğinde Evet'i seçin.
5. **Tanım** alanına bir değer girin.
6. **Kaydet**'e tıklayın.
7. **Konumları Seç**'i tıklatın.
8. Listede, seçili satırı işaretleyin.
9. **Ölçütler** alanından bir değer seçin.
10. **Tamam**'a tıklayın.
11. Sayfayı kapatın.

## <a name="create-a-cycle-count-plan"></a>Bir döngü sayım planı yaratın
1. **Gezinti bölmesinde**, **Modüller > ambar yönetimi > Kurulum > döngü sayımı > döngü sayısı planlarına** gidin.
2. **Yeni**'ye tıklayın.
3. **Döngü sayımı planı numarası** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Maksimum döngü sayımı miktarı** alanına bir sayı girin.
6. **Kaydet**'e tıklayın.
7. **Konumları Seç**'i tıklatın.
8. Listede, seçili satırı işaretleyin.
9. **Ölçütler** alanından bir değer seçin.
10. **Tamam**'a tıklayın.
11. **Döngü sayımları arasındaki günler** alanına bir sayı girin. Örneğin, **döngü sayımı alanında gün olarak belirtilen** değer 5 olarak ayarlanmışsa, her beş günde oluşturulur. Ancak, döngü sayımı işi üçüncü günde işleniyorsa, bir sonraki döngü sayımı işi son döngü sayımı işlendikten beş gün sonra, 8. gün içinde oluşturulur.  
12. **Kaydet**'e tıklayın.
13. **Yeni**'ye tıklayın.
14. **Sıra numarası** alanına bir numara girin. Sıralama en küçük sayıdan en büyük sayıyadır. Değer 0'dan (sıfır) fazla olmalıdır.  
15. Listede, seçili satırı işaretleyin.
16. **Tanım** alanına bir değer girin.
17. **Kaydet**'e tıklayın.
18. **Ürün sorgusu tanımla**'ya tıklayın.
19. Listede, seçili satırı işaretleyin.
20. **Ölçütler** alanında bir değer girin veya seçin.
21. **Tamam**'a tıklayın.
22. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]