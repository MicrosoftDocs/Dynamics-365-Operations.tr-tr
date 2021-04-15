---
title: Önceki sorunun yanıtına bağımlı bir soru hazırlama
description: Koşullu sorular, yanıtlayan kişinin önceki soruya verdiği cevaba göre hangi sorunun bir sonra sorulacağını belirlemenize olanak sağlar.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae4a792e53127196aacdf659bb483867d5c17494
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794745"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Önceki sorunun yanıtına bağımlı bir soru hazırlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Koşullu sorular, yanıtlayan kişinin önceki soruya verdiği cevaba göre hangi sorunun bir sonra sorulacağını belirlemenize olanak sağlar. Örneğin, "Kahve mi Çay mı tercih ediyorsunuz" sorusunu sorarsanız, yanıtlayanın cevapta çay mı kahve mi vermiş olduğuna göre mantıksal bir takip sorusu ile devam edebilirsiniz. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="find-the-existing-questionnaire"></a>Mevcut soru formunu bulun
1. Soru formu > Tasarım > Soru formları'na gidin.
2. Listede, WorkFH soru formunu seçin.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Soru formuna tüm soruları ve alt soruları ekleyin
1. Sorular'ı tıklatın.
2. Yeni'ye tıklayın.
3. Sorular alanında 00016 numaralı soruyu seçin.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Soru formu sırasını Koşullu olarak ayarlayın ve soruyu uygun soruya bağımlı hale getirin
1. Düzenle öğesine tıklayın.
2. Kurulum bölümünü genişletin.
3. Soru sıralaması alanında 'Koşullu' seçin.
4. Koşullu soru'ya tıklayın.
5. Ağaçta seçin 'Questions\Explain why you answered the previous question the way you did?'.
6. Birincil soru alanında 00009 numaralı soruyu seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Yanıt alanında, soruyu koşullandırmak istediğiniz yanıt seçeneğinin yanıt sıra kimliğini girin. Örneğin, ilk yanıt seçeneği için 1 girin.
9. Kaydet'i tıklatın.
10. Ağaçta 'Questions\I am paid fairly for the work I do.'.
    * Soru ağacının bağımlılığı göstermek için güncelleştirildiğinin farkına varın.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]