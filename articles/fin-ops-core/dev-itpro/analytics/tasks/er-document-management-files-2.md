---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2 - Veri modelini genişletme)
description: Aşağıdaki adımlar, bir Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd56ad01b00dfd0fe67f2d8eb36fb2bd39e04f1c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142610"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2 - Veri modelini genişletme)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1: Veri modelini hazırlama" görev kılavuzundaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>İçerdiği Belge Yönetimi dosyalarını sunmak için veri modelini genişletme
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.
4. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.
5. Tasarımcı'ya tıklayın.
6. Ağaçta "Müşteri fatura modeli(InvoiceCustomer)" seçeneğini işaretleyin.
    * Bu veri modelini, içerisindeki faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosyayı açığa çıkarmak için genişletiriz.  
7. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
8. Ad alanına "Fatura ekleri" yazın.
    * Fatura ekleri  
9. Madde türü alanında 'Kayıt listesi'ni seçin.
10. Ekle öğesini tıklatın.
11. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
12. Ad alanına "Dosya içeriği" yazın.
    * Dosya içeriği  
13. Madde türü alanında "Konteyner" öğesini seçin.
14. Ekle öğesini tıklatın.
15. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
16. Ad alanına "Dosya adı" yazın.
    * Dosya adı  
17. Madde türü alanında 'Dize' seçin.
18. Ekle öğesine tıklayın.

## <a name="map-new-data-model-elements-to-data-sources"></a>Veri kaynaklarına yeni veri modeli öğelerini eşleme
1. Modeli veri kaynağına eşle'yi tıklayın.
2. Açıklama alanına bir "InvoiceCustomer" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
    * InvoiceCustomer  
    * Uygun veri kaynaklarına yeni model öğeleri eşleriz.  
3. Tasarımcı'yı tıklatın.
4. Ağaçta "Fatura ekleri" seçeneğini işaretleyin.
5. Ağaçta, "Fatura ekleri" seçeneğini genişletin.
6. Ağaçta, "Fatura ekleri\Dosya adı" seçeneğini işaretleyin.
7. Düzenle öğesine tıklayın.
8. Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' yazın.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Kaydet'e tıklayın.
10. Sayfayı kapatın.
11. Ağaçta, "Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.
12. Düzenle öğesine tıklayın.
13. Formül alanına, '>CustInvoiceJour.'<Relations'.SalesTable.'Relations'.'<Documents'.'getFileContentAsContainer()'' yazın.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
16. Ağaçta "Fatura ekleri" seçeneğini işaretleyin.
17. Düzenle öğesine tıklayın.
18. Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' yazın.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.
21. Kaydet'e tıklayın.
22. Sayfayı kapatın.
23. Sayfayı kapatın.
24. Sayfayı kapatın.
25. Durumu değiştir öğesine tıklayın.
26. Tamamla öğesine tıklayın.
27. Tamam'a tıklayın.

