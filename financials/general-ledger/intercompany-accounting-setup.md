---
title: "Şirketlerarası Hesap Kurulumu"
description: "Bu konu, defter tahsisleri ve günlük günlüklerini, Satıcı Fatura günlükleri ve ödeme günlükleri gibi mali günlükler için şirketlerarası günlükleri kullanabilirsiniz böylece şirketlerarası muhasebesi ayarlama açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Şirketlerarası Hesap Kurulumu

Bu konu, defter tahsisleri ve günlük günlüklerini, Satıcı Fatura günlükleri ve ödeme günlükleri gibi mali günlükler için şirketlerarası günlükleri kullanabilirsiniz böylece şirketlerarası muhasebesi ayarlama açıklar.

Şirketlerarası günlükleri çeşitli senaryolarda olduğu gibi günlük günlüklerin, Satıcı Fatura günlükleri, genel muhasebe Tahsisatlar ve merkezi ödemeler için oluşturulabilir. Bu senaryoları etkinleştirmek için şirketler arası muhasebeyi kurmanız gerekir.

## <a name="define-main-accounts"></a>Ana hesaplarını tanımlayın
İlk olarak, Vade sonu ve Vade başlangıcı hesap girişleri için kullanılmak üzere şirketler arası ana hesaplar oluşturmanız gerekir. Şirketler arası muhasebe girişlerinin mutabakatını ve eliminasyonunu basitleştirmek amacıyla her bir şirket için özgün ana hesapların kullanılması iyi bir fikirdir. Şirketlerarası şirketlerin tanıtmak için bir ticaret ortağı veya karşılık gelen boyut kullanıyorsanız, Şirketlerarası muhasebede tanımlanan ana hesap üzerinde sabit bir boyut olarak bu boyut tanımlayabilirsiniz. Ana hesapları ayarladığınızda, ayarlamanız gerekir **ana hesap türü** alanı **Bilanço** üzerinde **ana hesaplar** sayfa.

## <a name="define-journal-names"></a>Günlük adları tanımlama
Ardından, bir günlük adı tanımlamalısınız. Set **günlük türü** alanı **günlük** üzerinde **günlük adları** sayfa. Şirketler arası muhasebe için özel bir günlük adı kullanmak iyi bir fikirdir.

## <a name="define-intercompany-accounting-setup"></a>Şirketlerarası hesap kurulumu tanımlayın
**Şirketlerarası muhasebe** sayfa birbirleri ile transact tüzel kişilikler çiftleri oluşturmak için kullanılır. Şirketlerarası hesap kurulum Kur tüm tüzel kişilikler görünür olacak şekilde paylaşılır. Yeni bir tüzel kişilik çifti oluştururken, hangi bir tüzel kişilik kaynak şirketini hedef şirket karşılık olarak tanımlanır farkında olduğunuzdan emin olun. Şirketlerarası hareketleri girerken, hareketin hangi bir tüzel kişilik başlatma veya hareket kaynaklanan belirler. Örneğin, şirketlerarası muhasebe USMF (kaynak) ve USSI (hedef) için ayarlanır. Kullanıcı etkin USSI ve USMF içeren şirketlerarası bir hareket girer, yalnızca şirketlerarası muhasebe için USMF tanımlanmadığı için hareket kaynağı olan deftere nakletmez. Bir hareket her iki şirket kaynaklanan karşılıklı kurulum için ikinci bir tüzel kişilik çifti oluşturmak gerekecektir. 

Seçin **Borç hesabı (ödeyeceği)** ve **kredi hesabına (son)** için hem kaynak hem de hedef tüzel kişilik. Tanımladığınız **günlük adı** hedef şirkette hareketi oluşturulurken kullanılacak. Günlük kaynak şirket için şirketlerarası hareket oluştururken, kullanıcı tarafından seçilen çünkü zaten biliniyor. 

Son olarak, muhasebe, nakit iskontosu veya Gerçekleşmiş kazançları/zararları merkezi ödeme tutarları desteklemek için hangi bir tüzel kişilik alacağını seçin. 

Karşılıklı ilişki kolayca üzerinde ayarlanabilir **Şirketlerarası muhasebe** kullanarak sayfayı **karşılıklı ilişki oluşturmak** ilk tüzel çifti oluşturulduktan sonra düğme. Karşılıklı çifti oluşturulduğunda, şirkete kaynak ve hedef şirket için bilgiler kopyalanır. Hedef şirket için tanımlanan günlük kalacak. Günlük adının aynı olması çoğu kuruluş için günlük adları, aynı adlandırma kuralını kullanın. Günlük adı farklı ise, alanında bulunan günlük yok ve çeşitli günlük seçili bildiren bir uyarı görüntülenir.


