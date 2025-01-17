Archive Attribute Coercion
==========================
Archive Attribute Coercion of received/sent DIMSE

.. tabularcolumns:: |p{4cm}|l|p{8cm}|
.. csv-table:: Archive Attribute Coercion Attributes (LDAP Object: dcmArchiveAttributeCoercion)
    :header: Name, Type, Description (LDAP Attribute)
    :widths: 23, 7, 70

    "
    .. _cn:

    :ref:`Name <cn>`",string,"Arbitrary/Meaningful name of the Archive Attribute Coercion

    (cn)"
    "
    .. _dcmDIMSE:

    :ref:`DIMSE <dcmDIMSE>`",string,"DICOM Message Element on which this Attribute Coercion shall be applied Enumerated values: N_CREATE_RQ, C_STORE_RQ, C_FIND_RQ or C_FIND_RSP.

    (dcmDIMSE)"
    "
    .. _dicomTransferRole:

    :ref:`DICOM Transfer Role <dicomTransferRole>`",string,"DICOM Transfer Role of peer DICOM AE. Enumerated values: SCU or SCP.

    (dicomTransferRole)"
    "
    .. _dcmRulePriority:

    :ref:`Rule Priority <dcmRulePriority>`",integer,"Rule Priority.

    (dcmRulePriority)"
    "
    .. _dcmAETitle:

    :ref:`AE Title(s) <dcmAETitle>`",string,"Application Entity (AE) title of peer DICOM AE for which this Attribute Coercion shall be applied. Apply on any if absent.

    (dcmAETitle)"
    "
    .. _dcmHostname:

    :ref:`Hostname(s) <dcmHostname>`",string,"DNS hostname of peer DICOM AE for which this Attribute Coercion shall be applied. Apply on any if absent.

    (dcmHostname)"
    "
    .. _dcmSOPClass:

    :ref:`SOP Class UID(s) <dcmSOPClass>`",string,"UID of SOP Class for which this Attribute Coercion shall be applied. Apply on any if absent.

    (dcmSOPClass)"
    "
    .. _dcmRetrieveAsReceived:

    :ref:`Retrieve as Received <dcmRetrieveAsReceived>`",boolean,"Disables merge of DB information into the retrieved Composite Object, returning the objects as received. Only effective with DIMSE = C_STORE_RQ and DICOM Transfer Role = SCP.

    (dcmRetrieveAsReceived)"
    "
    .. _dcmDeIdentification:

    :ref:`De-identification(s) <dcmDeIdentification>`",string,"De-identify objects according the Basic Application Level Confidentiality Profile specified in DICOM PS3.15. Selecting any Option implicitly includes the Basic Application Level Confidentiality Profile. Enumerated values: BasicApplicationConfidentialityProfile, RetainLongitudinalTemporalInformationFullDatesOption, RetainDeviceIdentityOption, RetainInstitutionIdentityOption or RetainUIDsOption.

    (dcmDeIdentification)"
    "
    .. _dcmURI:

    :ref:`XSL Stylesheet URI <dcmURI>`",string,"Specifies URI of the XSL style sheet for Attribute Coercion

    (dcmURI)"
    "
    .. _dcmNoKeywords:

    :ref:`No Attribute Keyword <dcmNoKeywords>`",boolean,"Indicates if attribute keywords shall be omitted in DICOM XML passed to XSLT

    (dcmNoKeywords)"
    "
    .. _dcmMergeMWLMatchingKey:

    :ref:`Merge MWL Matching Key <dcmMergeMWLMatchingKey>`",string,"Specifies attribute of received object to lookup MWL Item used to coerce request attributes. If absent, request attributes of received objects will not be coerced. Enumerated values: AccessionNumber, StudyInstanceUID or ScheduledProcedureStepID.

    (dcmMergeMWLMatchingKey)"
    "
    .. _dcmMergeMWLTemplateURI:

    :ref:`Merge MWL Template URI <dcmMergeMWLTemplateURI>`",string,"Specifies URI for the style sheet to coerce request attributes of received objects from matching DICOM MWL items. Only effective, if dcmMergeMWLMatchingKey is specified.

    (dcmMergeMWLTemplateURI)"
    "
    .. _dcmLeadingCFindSCP:

    :ref:`Leading C-FIND SCP <dcmLeadingCFindSCP>`",string,"AE Title of external C-FIND SCP for Attribute Coercion with Patient and Study attributes fetched from this AE. If no particular Attribute Set is specified for the C-FIND SCP, all Attributes of the configured Patient and Study Attribute Filter will be fetched.

    (dcmLeadingCFindSCP)"
    "
    .. _dcmAttributeUpdatePolicy:

    :ref:`Attribute Update Policy <dcmAttributeUpdatePolicy>`",string,"Specifies how attributes shall be updated with attributes fetched from Leading C-FIND SCP. PRESERVE (= nullify attributes in the new dataset which are not present in the original dataset), SUPPLEMENT (= attributes not present in original dataset will be supplemented), REPLACE (= original dataset is completely replaced), MERGE (= attribute values will be written from new dataset), OVERWRITE (= attribute values if null in new dataset, will be nullified in original dataset) Enumerated values: PRESERVE, SUPPLEMENT, MERGE, REPLACE or OVERWRITE.

    (dcmAttributeUpdatePolicy)"
    "
    .. _dcmNullifyTag:

    :ref:`Nullify Attribute Tag(s) <dcmNullifyTag>`",string,"DICOM Tag of Attribute to be nullified as hex string

    (dcmNullifyTag)"
    "
    .. _dcmNullifyIssuerOfPatientID:

    :ref:`Nullify Issuer of Patient ID <dcmNullifyIssuerOfPatientID>`",string,"Conditionally nullify Issuer of Patient ID (0010,0021) and Issuer of Patient ID Qualifiers Sequence (0010,0024) from received objects Enumerated values: ALWAYS, MATCHING or NOT_MATCHING.

    (dcmNullifyIssuerOfPatientID)"
    "
    .. _dcmIssuerOfPatientID:

    :ref:`Issuer of Patient ID(s) <dcmIssuerOfPatientID>`",string,"Issuer of Patient ID (0010,0021), and optionally also values for the Universal Entity ID (0040,0032) and the Universal Entity ID Type (0040,0033) of the Item of the Issuer of Patient ID Qualifiers Sequence (0010,0024) against values in received objects are matched, if Nullify Issuer of Patient ID is set to MATCHING or NOT_MATCHING. Format: <Issuer of Patient ID> [& <Universal Entity ID> & <Universal Entity ID Type>].

    (dcmIssuerOfPatientID)"
    "
    .. _dcmIssuerOfPatientIDFormat:

    :ref:`Issuer Of Patient ID Format <dcmIssuerOfPatientIDFormat>`",string,"Format of Issuer of Patient ID (0010,0021) derived from other attributes. E.g. ""{00100010,hash}-{00100030}"": use hash value of Patient Name and Birth Date separated by ""-"". For coercion of existing values of Issuer of Patient ID in received objects also dcmNullifyIssuerOfPatientID must be set accordingly.

    (dcmIssuerOfPatientIDFormat)"
    "
    .. _dcmSupplementFromDeviceName:

    :ref:`Supplement from Device <dcmSupplementFromDeviceName>`",string,"Name of Device from which Assigning Authorities and other information is taken to supplement received Composite Objects and MPPS.

    (dcmSupplementFromDeviceName)"
