---
title: Kalite emirlerini ayarlama
description: Bu prosedürde, size, gelen stoğun varış kaydı yapıldıktan hemen sonra incelenmesi gerektiği durumlarda kalite yönetim işleminin nasıl etkinleştirileceği gösterilmektedir.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 875d79e33fbd1d3d811d93dea98fa9d490716744
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011484"
---
# <a name="set-up-quality-orders"></a>Kalite emirlerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu prosedürde, size, gelen stoğun varış kaydı yapıldıktan hemen sonra incelenmesi gerektiği durumlarda kalite yönetim işleminin nasıl etkinleştirileceği gösterilmektedir. Bu prosedür genellikle bir kalite yöneticisi tarafından gerçekleştirilir. İşlem, örnek alınacak maddeleri tanımlamak üzere bir kalite grubu oluşturmayı ve kalite grubundaki maddeler üzerinde uygulanacak testleri gruplandırmak üzere bir test grubu oluşturmayı içerir. USMF demo veriler şirketinde bu kılavuzu çalıştırabilirsiniz.


## <a name="enable-quality-management"></a>Kalite yönetimini etkinleştirme
1. **Gezinme bölmesi > Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.
2. **Kalite yönetimi** sekmesine tıklayın.
3. **Kalite yönetimini kullan seçeneğini** "Evet" konumuna ayarlayın.
4. **Rapor kurulumu**'na tıklayın. USMF'de, kalite yönetimi için rapor kurulumu zaten tanımlıdır. Bu yapılmadıysa farklı rapor türleri için buraya yeni satırlar eklemeli ve her bir rapor için kullanılacak belge türünü seçmelisiniz.  
5. Sayfayı kapatın.
6. Sayfayı kapatın.

## <a name="create-a-test"></a>Test oluşturun
1. **Stok yönetimi > Kurulum > Kalite kontrol > Testler** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Test** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Tür** alanında, "Seçenek"i seçin. Bu örnekte, test sonuçlarını önceden tanımlanmış değerler temel alınarak atamayı olanaklı hale getiren "Seçenek"i seçeceğiz.  
6. **Kaydet**'e tıklayın.
7. Sayfayı kapatın.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Test sonuçlarını kaydetme şeklini tanımlamak için Test değişkenleri oluşturun
1. **Stok yönetimi > Kurulum > Kalite kontrol > Test değişkenleri** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Değişken** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Kaydet**'e tıklayın.
6. **Sonuçlar**'a tıklayın.
7. **Yeni**'ye tıklayın.
8. **Sonuç** alanına bir değer girin.
9. **Tanım** alanına bir değer girin.
10. **Sonuç durumu** alanında, "Başarılı"yı seçin.
11. **Kaydet**'e tıklayın.
12. **Yeni**'ye tıklayın.
13. **Sonuç** alanına bir değer girin.
14. **Tanım** alanına bir değer girin.
15. **Kaydet**'e tıklayın.
16. Sayfayı kapatın.
17. Sayfayı kapatın.

## <a name="set-up-item-sampling"></a>Madde örneklemesi ayarlayın
1. **Stok yönetimi > Kurulum > Kalite kontrol > Madde örnekleme** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Madde örnekleme** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Değer** alanına bir sayı girin. Bu değer bitişik alanda seçilen Miktar belirtimiyle ilgilidir.  
6. **İşlem** bölümünü genişletin veya daraltın.
7. **Tam durdurma** onay kutusunu işaretleyin veya işaretini kaldırın. Bu seçeneği belirtirseniz, bir test başarısız olduğu zaman tüm lot veya sipariş satırı miktarı engellenir. Seçmezseniz, yalnızca kalite emrindeki maddeler engellenir.  
8. **Kaydet**'e tıklayın.
9. Sayfayı kapatın.

> [!NOTE]
> *Ambar işlemleri için kalite yönetimi* özelliği bazı ek madde örnekleme yetenekleri sağlar. *Madde örnekleme kapsamı* kavramı ve miktar belirtimi olarak tam plaka tanımlama yeteneği ekler. Bu özelliği etkinleştirdiyseniz, ayrıntılar için [Ambar işlemleri için kalite yönetimi](../quality-management-for-warehouses-processes.md)'ne bakın.

## <a name="create-a-quality-group"></a>Kalite grubu oluşturun
1. **Stok yönetimi > Kurulum > Kalite kontrol > Kalite grupları** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Kalite grubu** alanına bir değer girin. Grupta hangi tür maddelerin (örnekleme ölçütlerinizin) yer alacağını bilmenize yardımcı olacak açıklayıcı bir ad kullanın.  
4. **Tanım** alanına bir değer girin.
5. **Kaydet**'e tıklayın.
6. **Madde ekle**'yi tıklatın.
7. **Madde numarası** satırını seçin. Bu örnekte filtreleme madde numarasına göre yapılacak.  
8. **Ölçütler** alanına bir değer yazın. Örneğin, T harfiyle başlayan madde numaralarını filtrelemek için T* yazın.  
9. **Tamam**'a tıklayın.
10. **Tamam**'a tıklayın.
11. **Madde kalite gruplarına** tıklayın.
12. Sayfayı kapatın.
13. Sayfayı kapatın.

## <a name="create-a-test-group"></a>Test grubu oluşturma
1. **Stok yönetimi > Kurulum > Kalite kontrol > Test grupları** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Test grubu** alanına bir değer girin. **Test grubuna**, ne tür testlerin çalıştırılmakta olduğunu ve grubun hangi kalite grubuyla ilişkilendirileceğini hatırlamanıza yardımcı olacak bir ad verin. Örneğin "T" harfiyle başlayan maddeleri seçen bir kalite grubuyla kullanılacaksa, gruba "T-madde testleri" adı verebilirsiniz.  
4. **Tanım** alanına bir değer girin.
5. **Madde örnekleme** alanında, önceden oluşturduğunuz madde örnekleme satırını seçin.
6. Listede, istenen kaydı bulun ve seçin.
7. **Ekle** öğesine tıklayın.
8. **Sıra numarası** alanına bir numara girin.
9. **Test** alanında, daha önce oluşturduğunuz testi seçin.
10. Listede, istenen kaydı bulun ve seçin.
11. **Test** sekmesine tıklayın.
12. **Değişken** alanında, daha önce oluşturduğunuz test değişkenini seçin.
13. Listede, istenen kaydı bulun ve seçin.
14. **Varsayılan sonuç** alanında, açılır menü düğmesine tıklayarak aramayı açın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
16. **Kaydet**'e tıklayın.
17. Sayfayı kapatın.

## <a name="define-when-quality-orders-will-be-created"></a>Kalite emirlerinin ne zaman oluşturulacağını tanımlayın
1. **Stok yönetimi > Kurulum > Kalite kontrol > Kalite ilişkileri** öğesine gidin.
2. **Yeni**'ye tıklayın.
3. **Referans türü** alanında bir seçenek belirtin.
4. **Madde kodu** alanında, "Grup"u seçin. Bu örnekte, "Grup"u seçeceğiz ve daha önce oluşturduğumuz kalite grubunu kullanacağız. Ayrıca, maddeleri el ile belirtmek için ayarını "Tablo" yapabilir veya kalite emrine tüm maddeleri eklemek için "Tümü"nü seçebilirsiniz.  
5. **Madde** alanında, önceden oluşturduğunuz kalite grubunu seçin. Madde alanındaki kullanılabilir seçenekler, Madde kodu alanındaki ayarlarınıza bağlıdır.  
6. Listede, istenen kaydı bulun ve seçin.
7. İşlem bölümünü genişletin veya daraltın.
8. **Olay türü** alanında bir seçenek belirtin. Bu, testi tetikleyen olaydır. Buradaki kullanılabilir seçenekler Başvuru türü alanında seçtiğiniz işleme bağlıdır.  
9. **Yürütme** alanında bir seçenek belirtin.
10. **Kalite emri işlemi** bölümünü genişletin veya daraltın.
11. **Olay durdurma** alanında, açılır menü düğmesine tıklayarak aramayı açın. Bu alanda, kalite emri hala açıksa, engellenebilecek işlemlerin listesi gösterilmektedir. Seçenekler, Olay türü alanındaki seçimlerinize bağlıdır.  
12. Listede, seçili satırdaki bağlantıya tıklayın. Bu, önceden seçtiğiniz değerlere bağlı olacaktır. Bir kaynak belge satırıyla bağlantılı açık kalite emirleri varken, izleyen işlemlerin engellenip engellenmemesi gerektiğini belirtin.  
13. **Belirtimler** bölümünü genişletin veya daraltın.
14. **Test grubu** alanında, daha önce oluşturduğunuz test grubunu seçin.
15. Listede, istenen kaydı bulun ve seçin.
16. **Kaydet**'e tıklayın.
17. Sayfayı kapatın.

> [!NOTE]
> *Ambar işlemleri için kalite yönetimi* özelliği, kalite ilişkilerini ayarlamak için ek seçenekler sağlar. Yeni bir koşul (**Geçerli ambar türü**) ve yeni bir ayar (**Kalite işleme ilkesi**) ekler. Bu özelliği etkinleştirdiyseniz, ayrıntılar için [Ambar işlemleri için kalite yönetimi](../quality-management-for-warehouses-processes.md)'ne bakın.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]