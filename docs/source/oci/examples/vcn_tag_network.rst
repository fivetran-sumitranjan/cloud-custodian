.. _vcntagnetwork:

VCN - Tag all the VCN in the tenancy
====================================

The following example policy will tag all the VCN in the tenancy

.. code-block:: yaml

    policies:
    - name: tag-vcn
      description: |
        Tag all the VCN in the tenancy
      resource: oci.vcn
      actions:
       - type: update-vcn
         params:
           update_vcn_details:
             freeform_tags:
               TagName: TagValue
