---
title: Bağlı şirket verilerini dosyalardan içeri aktarma
description: Bu makalede, Microsoft Dynamics 365 Finance'e içeri aktarılabilmesi için harici sistemlerdeki verilerin nasıl hazırlanacağı açıklamaktadır.
author: jinniew
ms.date: 10/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 494f6396d5e6fab6fef9404ad473566b02b1b9ab
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780109"
---
# <a name="import-subsidiary-data-from-files"></a>Bağlı şirket verilerini dosyalardan içeri aktarma

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Finance'e içeri aktarılabilmesi için harici sistemlerdeki verilerin nasıl hazırlanacağı açıklamaktadır. Harici sistemlerden bağlı şirket verilerinin aktarımını hazırlamak için **İçeri aktarma ile konsolide et** sayfasını (**Konsolidasyonlar \> İçeri aktarma ile konsolide et**) kullanın.

1. Konsolidasyon için bağlı şirket tüzel kişiliği oluşturun. Tüzel kişilik oluşturma hakkında bilgi için bkz. [Tüzel kişilik oluşturma](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Daha fazla bilgi için bkz [Konsolidasyon işleminde kullanılacak tüzel kişilik hazırlama](prepare-company-for-consolidation.md) ve [Konsolidasyon için bir alt şirket tüzel kişiliği ayarlama](set-up-subsidiary-company-for-consolidation.md).

2. İçeri aktarılan verileri içerecek bir dosya hazırlayın. İçeri aktarma işlemi hakkında daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. [Veri içeri/dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) içindeki "Veri içeri/dışarı aktarma işlemi" yordamındaki adımları izleyerek verileri bir dosyaya dışarı aktarın. Bu yordamı, verileri başka bir Dynamics 365 Finance örneğinden veya Dynamics 365 Business Central'dan verileri konsolide etmek için kullanabilirsiniz. Harici sistemlerden veri içeri aktarıyorsanız veriler [Alt şirket verilerini dosyalara dışarı aktarma](export-subsidiary-data-to-file.md) konusunda açıklanan biçimde olmalıdır.
4. **Konsolidasyonlar \> İçeri aktarma ile konsoli et**'e gidin. **İçeri aktarma ile konsolide et** sayfasında, **Ölçüt** sekmesinde, aşağıdaki alanları ayarlayarak raporun ve/veya içeri aktarmanın ayrıntılarını belirtin.

| Alan                                 | Rapor değeri | İçeri aktarma değeri |
|---------------------------------------|----------------------|----------------------|
| **Tanım**                      | Geçerli değil | İçeri aktarmayı tanımlayacak bir açıklama girin. |
| **Ana hesap**    | Raporun içermesi gereken hesap aralığını tanımlayın. Bir aralık tanımlamazsanız tüm hesaplar dahil edilir. | İçeri aktarmanın içermesi gereken hesap aralığını tanımlayın. Bir aralık tanımlamazsanız tüm hesaplar dahil edilir. |
    | **Konsolidasyon dönemi**                  | Konsolide edilecek tarih aralığını tanımlayın. | Konsolide edilecek tarih aralığını tanımlayın. |
    | **Gerçek tutarları dahil et**                | Fiili tutarları dahil etmek için bu seçeneği **Evet** olarak ayarlayın. | Fiili tutarları dahil etmek için bu seçeneği **Evet** olarak ayarlayın. |
| **Bütçe tutarlarını dahil et** | Bütçe tutarlarını konsolidasyona dahil etmek için bu seçeneği **Evet** olarak ayarlayın. | Bütçe tutarlarını konsolidasyona dahil etmek için bu seçeneği **Evet** olarak ayarlayın. |
| **Konsolidasyon sırasında bakiyeleri yeniden oluşturma** | Yeniden oluşturma işlemi bakiyeyi ve yeni kayıtları tamamen temizleyip bakiyeyi zamanın başlangıcından yeniden oluşturmak için bu seçeneği **Evet** olarak ayarlayın. | Yeniden oluşturma işlemi bakiyeyi ve yeni kayıtları tamamen temizleyip bakiyeyi zamanın başlangıcından yeniden oluşturmak için bu seçeneği **Evet** olarak ayarlayın. |
| **Bütçe modelleri**                         | Geçerli değil | Bütçe tutarlarını içeri aktarmayı seçtiyseniz konsolide edilecek bütçe modellerini girin. |
    | **Bütçe oran türü**                      | Geçerli değil | Bütçe döviz kurunun türünü girin. |

6. Farklı muhasebe para birimleriniz varsa konsolidasyon sırasında yapılan dönüşümü yapılandırmak için **Para birimi dönüşümü** sekmesindeki alanları kullanın.

    | Alan                      | Tanım |
    |----------------------------|-------------|
 | **Kaynak tüzel kişilik**        | İçeri aktarma kaynağı olarak kullanılan tüzel kişili seçin. |
 | **Kaynak muhasebe para birimi** | Bu varsayılan para birimi, **Kaynak tüzel kişilik** alanında seçtiğiniz kaynak tüzel kişilikle ilişkilendirilmiş para birimidir. |
 | **Kaynak** ve **Hedef hesaplar**       | Kaynak tüzel kişilikten içeri aktarılacak hesap aralığını tanımlayın. |
    | **Döviz kuru türü**         | Döviz kuru türünü seçin. Bir ana hesap oluşturduğunuzda Döviz Kuru türleri atanır. Daha fazla bilgi için bkz. [Ana hesap oluşturma](tasks/create-main-account.md). |
| **Şuradan döviz kurunu uygula**   | Bu tarihte geçerli olan döviz kurunun uygulanabilmesi için bir tarih girin. Alternatif olarak, döviz kuru olarak kullanılması gereken değeri girebilirsiniz. |
| **Döviz kuru**  | Varsayılan değer, **Döviz kuru türü** alanında seçtiğiniz döviz kuru türüne bağlıdır. Kullanıcı tanımlı bir döviz kuru girdiyseniz bir oran tanımlayabilirsiniz. |

7. İçeri aktarma işleminin arka planda çalışmasını sağlamak için **Arka planda çalıştır** seçeneğini **Evet** olarak ayarlayın.
8. Konsolidasyonu belirli bir zamanda toplu iş olarak çalıştırmak için **Toplu İşleme** seçeneğini **Evet** olarak ayarlayın. Konsolidasyonu hemen çalıştırmak için **Tamam**'ı seçin. 

Bağlı şirketlerde konsolidasyon için belirtilen hareket ve bakiyeler, ilgili konsolide edilen tüzel kişilikteki uygun hesaplara eklenir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
