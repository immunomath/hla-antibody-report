---
canonical: https://fhir.nmdp.org/ig/HLAAntibodyReport/StructureDefinition/HLAAntibodyReportBundle
expand: 2
---

# {{page-title}}

## Metadata

These are the details for this resource:

<fql output="table">
	from
		StructureDefinition
	where
		url = %canonical
	select
		Name: name,
		Description: description,
		Canonical_URL: url,
		Status: status,
		Version: version
</fql>



## Resource content

These are different views on this resource:

<tabs>
<tab title="Overview">
	This is the tree view:
	{{tree, buttons}}
</tab>
<tab title="Detailed view">
	This is the detailed view:
	{{dict}}
</tab>
<tab title="XML">
	This is the resource in XML:
	{{xml}}
</tab>
<tab title="JSON">	
	This is the resource in JSON:
	{{json}}
</tab>
<tab title="Link">
	{{link}}
</tab>
</tabs>

## Terminology Bindings

These are the terminology bindings within this resource:

<fql>
	from
    	StructureDefinition
	where
    	url = %canonical
	select
    	join for differential.element
      		select {
				Path: id,
				join
				for binding
				where valueSet.exists()
				select {
					Conformance: strength,
					ValueSet: valueSet}
        	}
</fql>

## Constraints

These are the constraints (invariants) defined within this resource:

<fql>
    from
		StructureDefinition
    where
		url = %canonical
    select
		differential.element {
			Path: id,
			join constraint {
				Id: key,
				Grade: severity,
				Details: human,
				Expression: expression
				}
			}
</fql>

### Class Diagram

<plantuml>
  set namespaceSeparator none
  skinparam backgroundcolor transparent

   class "Patient" <<Patient>>
    {
      labRefId = 156784
      name = Withheld
    }
 class "HLA Antibody Diagnostic Report" <<HLAAntibodyDiagnosticReport>>
    {
      DiagnosticReportId = 1937364874673
    }
 class "Laboratory-Organization" <<Laboratory>>
    {
      laboratoryId = 12393712
      name = HLA Laboratory
    }
  class "Working Sample" <<WorkingSample>>
    {
      workingSampleId = 3739373468
      patientSpecimenId = 4343847748
    }
  class "Immunoassay Kit" <<ImmunoAssayKit>>
    {
      deviceId = 100238373678
    }
  class ImmunoassayInterpretation <<Interpretation>>
    {
      negative-specificities = "HLA-A*01:01:01:01+HLA-A*24:02:01:01"
      positive-specificities = "HLA-A*01:01:01:01+HLA-A*24:02:01:01"
      questionable-specificities = "HLA-A*01:01:01:01+HLA-A*24:02:01:01"
    }
  class ImmunoassayBeadObservation1 <<Bead>>
    {
      beadId = 1001
      raw_mfi = 7650
      converted_mfi = 7500
    }
  class ImmunoassayBeadControlNeg1 <<NegativeControlBead>>
    {
      beadId = 1002
      raw_mfi = 650
      converted_mfi = 500
    }
  class ImmunoassayBeadControlPos1 <<PositiveControlBead>>
    {
      beadId = 1002
      raw_mfi = 6850
      converted_mfi = 8500
    }
  class ImmunoassayBeadObservation2 <<Bead>>
    {
      beadId = 1005
      raw_mfi = 7650
      converted_mfi = 7500
    }
  class ImmunoassayBeadControlNeg2 <<NegativeControlBead>>
    {
      beadId = 1006
      raw_mfi = 650
      converted_mfi = 500
    }
  class ImmunoassayBeadControlPos2 <<PositiveControlBead>>
    {
      beadId = 1007
      raw_mfi = 6050
      converted_mfi = 6000
    }
  class ImmunoassayBeadControlSerum1 <<PositiveControlSerum>>
    {
      specimenId = 10072433
    }    
  class ImmunoassayBeadControlSerum2 <<NegativeControlSerum>>
    {
      specimenId = 10072434
    }    

  "Patient" <-- "HLA Antibody Diagnostic Report"
  "HLA Antibody Diagnostic Report" <-- "Laboratory-Organization"
  "HLA Antibody Diagnostic Report" <-- "Working Sample"
  "HLA Antibody Diagnostic Report" <-- "ImmunoassayInterpretation"
  "HLA Antibody Diagnostic Report" <-- "ImmunoassayBeadObservation1"
  "ImmunoassayBeadObservation1" <-- "Working Sample"
  "ImmunoassayBeadObservation1" <-- "ImmunoassayBeadControlNeg1"
  "ImmunoassayBeadObservation1" <-- "ImmunoassayBeadControlPos1"
  "ImmunoassayBeadControlNeg1" <-- "ImmunoassayBeadControlSerum1"
  "ImmunoassayBeadControlPos1" <-- "ImmunoassayBeadControlSerum2"
  "HLA Antibody Diagnostic Report" <-- "ImmunoassayBeadObservation2"
  "ImmunoassayBeadObservation2" <-- "Working Sample"
  "ImmunoassayBeadObservation2" <-- "ImmunoassayBeadControlNeg2"
  "ImmunoassayBeadObservation2" <-- "ImmunoassayBeadControlPos2"
  "ImmunoassayBeadControlNeg2" <-- "ImmunoassayBeadControlSerum1"
  "ImmunoassayBeadControlPos2" <-- "ImmunoassayBeadControlSerum2"

</plantuml>