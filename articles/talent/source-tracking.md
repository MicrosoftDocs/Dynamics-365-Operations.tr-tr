---
title: Aday profilleri ve başvurular için kaynakları izleme
description: Bu konu, aday profilleri ve uygulamaları için kaynağı izleme hakkında bilgi sağlar.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519338"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Aday profilleri ve başvurular için kaynakları izleme 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Bu konuda belirtilen işlev önizleme sürümünün bir parçası kullanılabilir. İçerik ve işlevde değişiklik yapılabilir. Bu özelliği kullanmak için bir yöneticinin Attract içinde **Yönetim ayarları**'nı kullanarak etkinleştirmesini isteyin. Gelecekteki bir sürüm kaynak izleme raporları sağlayacaktır. Daha fazla bilgi için bkz [Talent içinde önizleme özelliklerine erişin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

Adaylar bir işe başvurduğunda, Attract, otomatik olarak başvurunun kaynağını izler, size işe alma çabanızda yardımcı olacak değerli bilgiler sağlar. İşe alımcılar ve işe alma yöneticileri de bir adayı el ile bir işe veya yetenek havuzuna eklerken bir başvuru kaynağı seçebilirler.

**Etkinlik** sekmesi altında, başvuru etkinliği ayrıntılarında başvuru kaynağını görüntüleyebilirsiniz ve ayrıca, başvuru geçmişinde yetenek havuzları altında bulunan **Profil** içinde. Bir adayın profil kaynağını aday ayrıntıları altında **Profil** sekmesinde, her iki başvuru ve yetenek havuzunda bulabilirsiniz.

> [!NOTE] 
> İşlem şablonlarını [Kapsamlı işe alma eklentisinde](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring) bulabilirsiniz.

## <a name="pre-configured-sources"></a>Önceden yapılandırılmış kaynaklar

Varsayılan kaynak listesi, genel başvuru kaynaklarını içerir. Bazı kaynak türleri, örneğin **İş panosu** veya **Sosyal Ağ** gibi, ek kaynak ayrıntılarına sahiptir. Örneğin, **Sosyal Ağ**, Facebook ve Twitter'ı içerir. **Referans** kaynak türü, dahili bir çalışanı referans olarak belirtmenize olanak sağlar. Varsayılan kaynak listesi, aşağıdaki önceden yapılandırılmış kaynakları içerir:

-   Attract kariyer sitesi

-   Acente

-   Kariyer Fuarı

-   Şirket Pazarlaması

-   Konferanslar ve Fuarlar

-   Profesyonel İlişkilendirme

-   İş panosu

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Dergiler ve Yayınlar

-   Sosyal Ağ

    -   Facebook

    -   Twitter

-   Üniversiteden İşe Alma

-   LinkedIn

-   Seri İlanlar

-   Başvuru

-   İşe alımcı tarafından eklendi

-   Diğer

## <a name="customize-the-source-list"></a>Kaynak listesini özelleştir 

Kaynak listesini, ek başvuru kaynakları içermek üzere genişletebilirsiniz. Bu listeyi özelleştirmek için, [Attract içinde Seçenek Kümelerini Genişletmek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract) içindeki talimatları izleyin. **TalentSource** varlığını, ek kaynakları dahil etmek için düzenleyin. 

Kullanıcı arabirimini (UI) olumsuz etkilemekten kaçınmak için aşağıdakilerin **TalentCategory** enum değerlerini (isimleri değil) düzenlemeyi veya silmeyin:

- **Başvuru**
- **LinkedIn**
- **Diğer**

Bunun yerine, **TalentSource** enum'u diğer türde kaynaklar eklemek için genişletebilirsiniz.
