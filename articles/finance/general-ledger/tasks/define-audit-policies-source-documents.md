---
title: Kaynak belgeler için denetim ilkeleri tanımlama
description: Bu konu, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını açıklar.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836973"
---
# <a name="define-audit-policies-for-source-documents"></a>Kaynak belgeler için denetim ilkeleri tanımlama

[!include [banner](../../includes/banner.md)]

Bu konu, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını açıklar. Örnekte, otel gideri türünde gider raporları kullanılmaktadır. Bu yordam, USMF demo şirketini kullanır. Denetçi rolü bu görevleri gerçekleştirmek için uygun izinleri içerir.

1. Gezinti bölmesinde, **Modüller > Denetim çalışma ekranı > Kurulum > İlke kuralı türü**'ne gidin.
2. **Yeni**'yi seçin.
3. **Kural adı** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Sorgu adı** alanında **Gider raporu satırı** öğesini seçin
6. **Sorgu türü** alanında **Topla** öğesini seçin
7. **Tüzel kişilik** alanında **Tüzel kişilik** öğesini seçin
8. **Belge tarihi referansı** alanında **Değiştirilme tarihi ve saati** öğesini seçin
9. **Kaydet**'i seçin.
10. Gezinti bölmesinde, **Modüller > Denetim çalışma ekranı > Kurulum > Denetim ilkeleri**'ne gidin.
11. **Yeni**'yi seçin.
12. **Ad** alanına bir değer yazın.
13. **İlke organizasyonları**  bölümünü genişletin.
14. Ağaçta **Contoso Entertainment System USA** seçeneğini ve ardından **Ekle**'yi seçin.
15. Ağaçta **Contoso Consulting USA** seçeneğini ve ardından **Ekle**'yi seçin.
16. Ağaçta **Contoso Retail USA** seçeneğini ve ardından **Ekle**'yi seçin.
17. **İlke organizasyonları** bölümünü daraltın.
18. **İlke kuralları**  bölümünü genişletin.
19. Listede, önceden oluşturulmuş İlke Kuralı'nı bulup seçin.
20. **İlke kuralı oluştur**'u seçin.
21. **Yürürlük tarihi** alanına bir tarih ve saat girin.
22. **Filtre**'yi seç.
23. Listede, **Gider kategorisi** satırını seçin ve ayrıntıları **Otel** olarak ayarlayın
24. **Ölçütler** alanında bir değer girin veya seçin.
25. **Toplam** sekmesini seçin.
26. **Ekle**'yi seçin.
27. Listeden, **Hareket tutarı** için bir alan değeri seçin.
28. **Alan** alanında bir değer girin veya seçin.
29. **AggregateFunction** alanında **Toplam** seçeneğini seçin.
30. **Gruplandırma ölçütü** sekmesini seçin.
31. **Ekle**'yi seçin.
32. Listeden **Personel** için bir değer seçin.
33. **Ekle**'yi seçin.
34. Listeden **Gider kategorisi** için bir değer seçin.
35. **Alan** alanında bir değer girin veya seçin.
36. **Sahip** sekmesini seçin.
37. **Ekle**'yi seçin.
38. **Hareket tutarı**  öğesini seçin.
39. **Alan** alanında bir değer girin veya seçin.
40. **AggregateFunction** alanında **Toplam** seçeneğini seçin.
41. **Ölçütler** alanına `>2000` yazın.
42. **Tamam**'ı seçin.
43. **Test**'i seçin.
44. **Belge seçim başlangıç tarihi** alanına tarih ve saat girin.
45. **Belge seçim bitiş tarihi** alanına tarih ve saat girin.
46. **Testi çalıştır**'ı seçin.
47. Eylem Bölmesinde **Denetim ilkesi** öğesine tıklayın.
48. **Ek seçenekler** öğesini seçin.
49. **Başlangıç tarihi** alanına tarih ve saat girin.
50. **Bitiş tarihi** alanına tarih ve saat girin.
51. **Toplu iş**'i seçin.
52. **Arka planda çalıştır** bölümünü genişletin.
53. **Toplu işlem** alanında **Evet** seçeneğini seçin.
54. **Tamam**'ı seçin.
55. Gezinti bölmesinde **Modüller > Denetim çalışma ekranı > Denetim vakaları**'na gidin.
56. Listede, istenen kaydı bulun ve seçin.
57. **İlişkilendirmeler**  bölümünü genişletin.
58. Listede, istenen kaydı bulun ve seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]