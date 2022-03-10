---
title: Birden çok çalışma sayfasına sahip veri şablonları
description: Bu konu, Excel veri varlığı kullanarak Finans ve Operasyon içine veri içe aktarmayı açıklar.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: cf3c423bdf06685a3c4025551927123773ae818a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070073"
---
# <a name="data-templates-with-multiple-worksheets"></a>Birden çok çalışma sayfasına sahip veri şablonları

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Uygulamadaki veri yönetimi, veri varlıkları için Microsoft Excel tabanlı şablonları destekler. Bu şablonlar, bir veya daha fazla çalışma sayfası içerebilir. Birden çok çalışma sayfası içeren şablonlar genellikle verileri tek bir dosyada yönetmek ve dosyayı birden çok veri varlığına aktarmak uygun olduğunda kullanılır. Tesisler ve ambarlar bir örnek olabilir.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Önce bir dosya yükleyin ve bunu tüm varlıklarla eşleştirin
**Tesisler** ve **Ambarlar** adlı çalışma sayfaları içeren bir Excel dosyasının kullanıldığı bir örneği ele alalım. Veri içe aktarma projesini ayarlamak için öncelikle **Tesisler** veri varlığını ekler ve sonra dosyayı karşıya yüklersiniz. Bu varlık için kullanılacak çalışma sayfası olarak **Tesisler**'i seçebilirsiniz.

İkinci varlık olan **Ambarlar**'ı **Dosya Ekle** formunu kapatmadan seçerseniz, çalışma sayfası araması **Ambarlar** çalışma sayfasını dosyayı yeniden karşıya yüklemenize gerek kalmadan seçmenize olanak tanır. Yeni bir dosyayı karşıya yüklemenin tek nedeni **Ambarlar** verisinin farklı bir dosyada bulunması olabilir.

![Birden çok çalışma sayfası.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Çalışma sayfası ile varlık eşlemesini düzeltme

Çalışma sayfasının bir içe aktarma işinde veri varlığı eşlemesi kılavuzdan düzeltilebilir. Kılavuzdaki **Çalışma sayfası** sütunu eşlenen dosyadaki çalışma sayfalarını gösterir. Açılan menüden başka bir çalışma sayfasını seçebilirsiniz. Seçilen çalışma sayfası zaten veri projesindeki bir varlıkla eşlenmişse, sistem değişikliği onaylamanızı ister. Tüm eşlemeleri ızgarada düzeltmenizi öneririz.

![Çalışma sayfası eşlemesini güncelleştirme.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Yeni bir dosyayla yeniden eşleme

Veri projesindeki mevcut varlıklar için aynı dosyanın yeni bir sürümünün veya tamamen yeni bir dosyanın yüklenmesi gereken durumlarda, **Dosya ekle** deneyimini kullanmanız ve varlıkları sanki ilk kez ekleniyormuş gibi tekrar eklemeniz gerekir. Sistem devam etmeden önce veri projesindeki mevcut varlıkların üzerine yazmak istediğinizi onaylar. Tekrar eklenmeyen (veya üzerine yazılmayan) varlıklar önceki dosyadaki önceki eşlemeleri korumaya devam eder.

## <a name="upload-a-file-using-run-project"></a>Projeyi çalıştır özelliğini kullanarak dosya yükleme

Bir içe aktarma projesini yürütmek için **Projeyi çalıştır** seçeneğini kullanırken bir Excel dosyası yükleyebilirsiniz. Yalnızca veri projesinde yer alan veri varlıklarındaki mevcut eşlemelerle aynı çalışma sayfalarına sahip dosyaları yüklemeye dikkat etmeniz gerekir. Yeni yüklenen bir dosyada bir çalışma sayfası bulunamazsa, sistem bir hata görüntüler ve içe aktarma işlemini durdurur. Çalışma sayfası eşlemesinin bir varlık için değiştirilmesi gerekirse, **Projeyi çalıştır** seçeneğindeki dosya kullanılmadan önce ilk olarak veri projesindeki eşlemelerin veri projesi içinden güncelleştirilmesi gerekir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
