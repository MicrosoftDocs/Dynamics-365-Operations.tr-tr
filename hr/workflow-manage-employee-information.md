---
title: "Çalışan bilgilerini yönetmek için iş akışlarını kullanma"
description: "Bu konu, çalışan bilgilerini yönetmek için İnsan kaynakları için iş akışı özelliğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışı bir pozisyonla ilişkilendirmek ve çalışanların kendi kaydı değiştirdiğinizde, başlatılan bir onay iş akışı yapılandırın."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Çalışan bilgilerini yönetmek için iş akışlarını kullanma

Bu konu, çalışan bilgilerini yönetmek için İnsan kaynakları için iş akışı özelliğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışı bir pozisyonla ilişkilendirmek ve çalışanların kendi kaydı değiştirdiğinizde, başlatılan bir onay iş akışı yapılandırın.

İnsan kaynakları için iş akışı kapasitesi, İnsan Kaynakları faaliyetleri yönetmek için çok sayıda iş akışı sağlar. Ayrıca, belirli iş akışlarını değiştirin ve bunları raporlama hiyerarşisi ile ilişkilendirmek için çeşitli seçenekler kullanılabilir. Çalışan bilgileri birkaç standart türü değişiklikleri yönetmek iş akışları kullanılabilir. Bir iş akışı bir pozisyonla ilişkilendirebilirsiniz. Daha sonra çalışanların kendi çalışan kaydı değiştirirseniz, bir iş akışı yeni bilgiler kaydedilmeden önce onay gerektiren başlatılır. İş akışı bilgilerini değişiklikler etkili bir şekilde yönetmenize ve çalışanlarınızın verileri doğru tutmak yardımcı olmak için aşağıdaki türleri için önceden tanımlanmıştır:

-   Kimlik numaraları
-   Kurslar
-   Eğitim
-   Resim
-   Ödünç verilen maddeler
-   Mesleki deneyim
-   Proje deneyimi
-   Yetenekler
-   Güven gerektiren pozisyonlar
-   İnsan Kaynakları Eylemler
-   Kurs kayıt

Çalışanlar işe, transfer veya sona erdi, iş akışını gözden geçirme işleminin içerebilir. Bu şekilde, bir belgeyi gözden geçirilebilir veya eylem koşullarını iş akışının bir parçası tanımlanabilir. Gözden geçirme işlemi tamamlandığında, belge veya eylem tamamlandı ve iş akışını son onayı adım taşır.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Bir pozisyon hiyerarşide bir iş akışı ilişkilendirme
Bir iş akışı yapılandırdığınız herhangi bir hiyerarşi ilişkilendirebilirsiniz. Örneğin, bir pozisyon matris raporlama hiyerarşisi ile ilişkili ise, bir iş akışı Yöneticisi bu pozisyonla ilişkili çalışanı yerine Proje lideri giderler belirli bir proje için yönlendirir yapılandırmanız gerekebilir. Yeni bir iş akışı oluşturun veya varolan bir iş akışını değiştirmek için **İnsan Kaynakları iş akışı** sayfasında,'ı **yeni**. Bir iş akışı, iş akışı Tasarımcısı'nı başlatmak için listeden seçin. Tasarımcı, yeni bir iş akışı oluşturun veya varolan bir iş akışı adımlarını değiştirmek için kullanabilirsiniz. Varolan bir iş akışı değiştirdiğinizde, yaptığınız değişiklikleri yeni bir sürüm olarak kaydedilir. Gerekirse bu nedenle, her zaman önceki sürüme geri dönebilirsiniz.

## <a name="configure-a-human-resources-workflow"></a>İnsan Kaynakları iş akışı yapılandırma
Çalışanların kendi kişisel kimliğini değişiklik istediğinde, başlatılan temel iş akışı yapılandırmak için aşağıdaki adımları izleyin.

1.  Üzerinde **İnsan Kaynakları iş akışları** sayfasında,'ı **yeni**.
2.  Kullanılabilir iş akışları listesinden seçin **kimlik numaraları**.
3.  ' I **çalıştırmak** iş akışı Tasarımcısı'nı başlatın ve istendiğinde, kullanıcı adınızı ve parolanızı girin.
4.  Sürükleme **kimlik numarasını onaylamak** Tasarımcı tuval için iş akışı öğeleri listesinden öğe.
5.  Onay öğesine bağlanmak **Start** ve **son**.
6.  Çift **Onayla öğesi**ve sonra sağ tıklatın ve seçin **Özellikler**.
7.  İş öğesi yönergeleri eklemek için şu adımları izleyin:
    1.  Seçin **atama**ve sonra seçin **hiyerarşi** altında atama türü.
    2.  Altında **hiyerarşi** seçimi, select **yapılandırılabilir hiyerarşi**.
    3.  Bir durdurma koşulu ekleyin ve sayfayı kapatın.

8.  (Ek uyarı var olmalıdır) tüm ek yönergeleri izleyin.
9.  **Kaydet ve kapat**'ı tıklatın. İletişim kutusu açılır ve seçtiğinizde, yeni iş akışını etkinleştirip **etkin hale**.
10. Git **İnsan Kaynakları**&gt;**pozisyon**&gt;**yerleştirmek hiyerarşi türleri**.
11. Seçin **matris**.
12. Eklemek **çalışan kimlik numarası** listeye iş akışı.



