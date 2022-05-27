---
title: Planlamayı kullanarak soru formlarını dağıtma
description: Soru formu planlama, soru formlarınızı planlamanıza ve birden fazla alıcıya dağıtmanıza izin verir.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82f688a3d9366e629eedefd876dd5669bd7ed04
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691652"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Planlamayı kullanarak soru formlarını dağıtma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Soru formu planlama, soru formlarınızı planlamanıza ve birden fazla alıcıya dağıtmanıza izin verir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.

## <a name="create-a-questionnaire-schedule"></a>Soru formu planı oluşturma

1. **Soru formu** > **Dağıt** > **Soru formu planları**'nı seçin.

2. **Yeni**'yi tıklatın.

3. **Planlama** alanına bir değer yazın.

4. **Tanım** alanına bir değer girin.
    * İsimlerin yanıtlarla ilişkilendirilmeden kaydedilmesi gerekiyorsa planı **İsimsiz** konumuna ayarlayın.  
    * İK parametrelerinde ilk olarak anonim sonuçlara izin verme ayarlanmalıdır.  

5. **Tür** alanında planlama türünü seçin.  Bu örnekte **Memnuniyet** türünü kullanacağız.

6. Listede, istenen kaydı bulun ve seçin.

7. Listede, seçili satırdaki bağlantıya tıklayın.

8. **Tarih** alanına bir tarih girin.

9. **Çalışan self servis bölümü için e-posta**'yı genişletin.

10. **Konu** alanına bir değer yazın.

    * Örnek: Soru formu mevcut  

11. **Metin** alanına e-posta iletinizin gövdesini yazın. Sistemdeki değerleri değiştirmek için değişken kullanılabilir.

    * Örnek: Sayın %P%,  İşçi Sağlığı soru formunu tamamlamak için lütfen Personel Self Servisinde oturum açın.  Contoso  

12. **Kaydet**'e tıklayın.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Yanıtlanması gereken soru formlarını ve yanıtlayanların seçilmesinde kullanılacak sorguları seçmek için Kurulum ayrıntılarını kullanın.

1. **Kurulum ayrıntıları**'nı tıklayın.

2. Listede, soru formu için yanıtlayanları sistemde aramak üzere kullanmak için bir soru seçin.

    * Örnek: Çalışanlar  

3. Belirli kişileri seçmek veya sorguyu belirli bir ölçüte uyan kişileri bulmak için ayarlamak üzere **Sorguyu görüntüle veya değiştir** öğesine tıklayın.

    * Tüm yanıtlayanların sistemde ayrıca kullanıcı olmaları gerektiğini unutmayın.  

4. Listede, Kişi için satırı işaretleyin.

5. **Ölçütler** alanında bir değer girin veya seçin.

    * Julia Funderburk'ı seçin  

6. Listede, Julia Funderburk'u seçin

7. **Tamam**'a tıklayın.

8. **Soru formları** sekmesine tıklayın.

9. Ağaçta, "**Memnuniyet Anketi** soru formu türü düğümünü genişletin.

10. Ağaçta, "İşçi Sağlığı Değerlendirmesi" kutusunu işaretleyin.

11. **Tamam**'a tıklayın.

12. **Planlı yanıt oturumu**'na tıklayın.

    * **Planlı yanıt oturumlarının** her bir seçilen/sorgulanan kullanıcı için oluşturulduğuna dikkat edin.  

13. Sayfayı kapatın.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Soru formunu yanıtlayanlar tarafından tamamlanması için kullanılabilir hale getirmek üzere soru formu planını başlatın.

1. **İşlevler**'e tıklayın.

2. **Başlat**'a tıklayın.

3. **Tamam**'a tıklayın.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Mevcut soru formunu yanıtlayanları bilgilendirmek üzere e-posta gönderin.

1. **İşlevler**'e tıklayın.

2. **E-posta gönder**'e tıklayın.

3. **İptal**'e tıklayın

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Soru formunu tamamlaması gerekenleri izlemek için Planlı yanıt oturumları'nı kullanın.

1. **Planlı yanıt oturumu**'na tıklayın.

    * Planlı oturumu sonlandırmaya hazır duruma geldiğinizde varsa, kalan planlı yanıt oturumunu silin.  

2. **Sil** öğesini tıklayın.

3. **Evet** seçeneğini tıklatın.

4. Sayfayı kapatın.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Tüm yanıtlayanlar soru formunu tamamladığında ve/veya kalan tüm Planlı yanıt oturumları silindiğinde planı sonlandırın.

1. **İşlevler**'e tıklayın.
2. **Sonlandır**'ı tıklatın.
3. **Tamam**'a tıklayın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
