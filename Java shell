/**
 * Copyright (c) 2012, 2016 Sme.UP and others.
 * All rights reserved. This program and the accompanying materials
 * are made available under the terms of the Eclipse Public License v1.0
 * which accompanies this distribution, and is available at
 * http://www.eclipse.org/legal/epl-v10.html
 */
package org.smeup.sys.co.shell.impl;

import org.eclipse.emf.ecore.EClass;
import org.eclipse.emf.ecore.EGenericType;
import org.eclipse.emf.ecore.EOperation;
import org.eclipse.emf.ecore.EPackage;
import org.eclipse.emf.ecore.impl.EPackageImpl;
import org.smeup.sys.co.core.QCommunicationCorePackage;
import org.smeup.sys.co.shell.QCommunicationShellFactory;
import org.smeup.sys.co.shell.QCommunicationShellPackage;
import org.smeup.sys.co.shell.QShellCredentials;
import org.smeup.sys.co.shell.QShellData;
import org.smeup.sys.co.shell.QShellManager;
import org.smeup.sys.co.shell.QShellOutputWrapper;
import org.smeup.sys.il.data.QIntegratedLanguageDataPackage;
import org.smeup.sys.il.data.def.QIntegratedLanguageDataDefPackage;
import org.smeup.sys.il.data.term.QIntegratedLanguageDataTermPackage;
import org.smeup.sys.os.core.jobs.QOperatingSystemJobsPackage;
import org.smeup.sys.rt.auth.QRuntimeAuthenticationPackage;

/**
 * <!-- begin-user-doc --> An implementation of the model <b>Package</b>. <!--
 * end-user-doc -->
 * @generated
 */
public class CommunicationShellPackageImpl extends EPackageImpl implements QCommunicationShellPackage {
	/**
	 * <!-- begin-user-doc -->
	 * <!-- end-user-doc -->
	 * @generated
	 */
	private EClass shellCredentialsEClass = null;

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	private EClass shellOutputWrapperEClass = null;

	/**
	 * <!-- begin-user-doc -->
	 * <!-- end-user-doc -->
	 * @generated
	 */
	private EClass shellManagerEClass = null;

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	private EClass shellDataEClass = null;

	/**
	 * Creates an instance of the model <b>Package</b>, registered with
	 * {@link org.eclipse.emf.ecore.EPackage.Registry EPackage.Registry} by the
	 * package package URI value.
	 * <p>
	 * Note: the correct way to create the package is via the static factory
	 * method {@link #init init()}, which also performs initialization of the
	 * package, or returns the registered package, if one already exists. <!--
	 * begin-user-doc --> <!-- end-user-doc -->
	 *
	 * @see org.eclipse.emf.ecore.EPackage.Registry
	 * @see org.smeup.sys.co.shell.QCommunicationShellPackage#eNS_URI
	 * @see #init()
	 * @generated
	 */
	private CommunicationShellPackageImpl() {
		super(eNS_URI, QCommunicationShellFactory.eINSTANCE);
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	private static boolean isInited = false;

	/**
	 * Creates, registers, and initializes the <b>Package</b> for this model, and for any others upon which it depends.
	 * 
	 * <p>This method is used to initialize {@link QCommunicationShellPackage#eINSTANCE} when that field is accessed.
	 * Clients should not invoke it directly. Instead, they should simply access that field to obtain the package.
	 * <!-- begin-user-doc --> <!--
	 * end-user-doc -->
	 * @see #eNS_URI
	 * @see #createPackageContents()
	 * @see #initializePackageContents()
	 * @generated
	 */
	public static QCommunicationShellPackage init() {
		if (isInited) return (QCommunicationShellPackage)EPackage.Registry.INSTANCE.getEPackage(QCommunicationShellPackage.eNS_URI);

		// Obtain or create and register package
		CommunicationShellPackageImpl theCommunicationShellPackage = (CommunicationShellPackageImpl)(EPackage.Registry.INSTANCE.get(eNS_URI) instanceof CommunicationShellPackageImpl ? EPackage.Registry.INSTANCE.get(eNS_URI) : new CommunicationShellPackageImpl());

		isInited = true;

		// Initialize simple dependencies
		QCommunicationCorePackage.eINSTANCE.eClass();
		QRuntimeAuthenticationPackage.eINSTANCE.eClass();

		// Create package meta-data objects
		theCommunicationShellPackage.createPackageContents();

		// Initialize created meta-data
		theCommunicationShellPackage.initializePackageContents();

		// Mark meta-data to indicate it can't be changed
		theCommunicationShellPackage.freeze();

  
		// Update the registry and return the package
		EPackage.Registry.INSTANCE.put(QCommunicationShellPackage.eNS_URI, theCommunicationShellPackage);
		return theCommunicationShellPackage;
	}

	/**
	 * <!-- begin-user-doc -->
	 * <!-- end-user-doc -->
	 * @generated
	 */
	@Override
	public EClass getShellCredentials() {
		return shellCredentialsEClass;
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	@Override
	public EClass getShellOutputWrapper() {
		return shellOutputWrapperEClass;
	}

	/**
	 * <!-- begin-user-doc -->
	 * <!-- end-user-doc -->
	 * @generated
	 */
	@Override
	public EClass getShellManager() {
		return shellManagerEClass;
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	@Override
	public EClass getShellData() {
		return shellDataEClass;
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	@Override
	public QCommunicationShellFactory getCommunicationShellFactory() {
		return (QCommunicationShellFactory)getEFactoryInstance();
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	private boolean isCreated = false;

	/**
	 * Creates the meta-model objects for the package.  This method is
	 * guarded to have no affect on any invocation but its first.
	 * <!-- begin-user-doc -->
	 * <!-- end-user-doc -->
	 * @generated
	 */
	public void createPackageContents() {
		if (isCreated) return;
		isCreated = true;

		// Create classes and their features
		shellCredentialsEClass = createEClass(SHELL_CREDENTIALS);

		shellDataEClass = createEClass(SHELL_DATA);

		shellOutputWrapperEClass = createEClass(SHELL_OUTPUT_WRAPPER);

		shellManagerEClass = createEClass(SHELL_MANAGER);
	}

	/**
	 * <!-- begin-user-doc --> <!-- end-user-doc -->
	 * @generated
	 */
	private boolean isInitialized = false;

	/**
	 * Complete the initialization of the package and its meta-model. This
	 * method is guarded to have no affect on any invocation but its first. <!--
	 * begin-user-doc --> <!-- end-user-doc -->
	 *
	 * @generated
	 */
	public void initializePackageContents() {
		if (isInitialized) return;
		isInitialized = true;

		// Initialize package
		setName(eNAME);
		setNsPrefix(eNS_PREFIX);
		setNsURI(eNS_URI);

		// Obtain other dependent packages
		QRuntimeAuthenticationPackage theRuntimeAuthenticationPackage = (QRuntimeAuthenticationPackage)EPackage.Registry.INSTANCE.getEPackage(QRuntimeAuthenticationPackage.eNS_URI);
		QIntegratedLanguageDataTermPackage theIntegratedLanguageDataTermPackage = (QIntegratedLanguageDataTermPackage)EPackage.Registry.INSTANCE.getEPackage(QIntegratedLanguageDataTermPackage.eNS_URI);
		QIntegratedLanguageDataDefPackage theIntegratedLanguageDataDefPackage = (QIntegratedLanguageDataDefPackage)EPackage.Registry.INSTANCE.getEPackage(QIntegratedLanguageDataDefPackage.eNS_URI);
		QCommunicationCorePackage theCommunicationCorePackage = (QCommunicationCorePackage)EPackage.Registry.INSTANCE.getEPackage(QCommunicationCorePackage.eNS_URI);
		QIntegratedLanguageDataPackage theIntegratedLanguageDataPackage = (QIntegratedLanguageDataPackage)EPackage.Registry.INSTANCE.getEPackage(QIntegratedLanguageDataPackage.eNS_URI);
		QOperatingSystemJobsPackage theOperatingSystemJobsPackage = (QOperatingSystemJobsPackage)EPackage.Registry.INSTANCE.getEPackage(QOperatingSystemJobsPackage.eNS_URI);

		// Create type parameters

		// Set bounds for type parameters

		// Add supertypes to classes
		shellCredentialsEClass.getESuperTypes().add(theRuntimeAuthenticationPackage.getAuthenticationUserPassword());
		EGenericType g1 = createEGenericType(theIntegratedLanguageDataTermPackage.getDataTerm());
		EGenericType g2 = createEGenericType(theIntegratedLanguageDataDefPackage.getBufferedDataDef());
		g1.getETypeArguments().add(g2);
		EGenericType g3 = createEGenericType();
		g2.getETypeArguments().add(g3);
		shellDataEClass.getEGenericSuperTypes().add(g1);
		shellOutputWrapperEClass.getESuperTypes().add(theCommunicationCorePackage.getOutputWrapper());

		// Initialize classes and features; add operations and parameters
		initEClass(shellCredentialsEClass, QShellCredentials.class, "ShellCredentials", !IS_ABSTRACT, !IS_INTERFACE, IS_GENERATED_INSTANCE_CLASS);

		initEClass(shellDataEClass, QShellData.class, "ShellData", !IS_ABSTRACT, !IS_INTERFACE, IS_GENERATED_INSTANCE_CLASS);

		initEClass(shellOutputWrapperEClass, QShellOutputWrapper.class, "ShellOutputWrapper", IS_ABSTRACT, IS_INTERFACE, IS_GENERATED_INSTANCE_CLASS);

		initEClass(shellManagerEClass, QShellManager.class, "ShellManager", IS_ABSTRACT, IS_INTERFACE, IS_GENERATED_INSTANCE_CLASS);

		EOperation op = addEOperation(shellManagerEClass, theIntegratedLanguageDataPackage.getDataContainer(), "decodeCommand", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, theOperatingSystemJobsPackage.getJobCapability(), "capability", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, ecorePackage.getEString(), "command", 1, 1, IS_UNIQUE, IS_ORDERED);

		op = addEOperation(shellManagerEClass, ecorePackage.getEString(), "encodeCommand", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, theOperatingSystemJobsPackage.getJobCapability(), "capability", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, theIntegratedLanguageDataPackage.getDataContainer(), "container", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, ecorePackage.getEBoolean(), "showDefaults", 0, 1, IS_UNIQUE, IS_ORDERED);

		op = addEOperation(shellManagerEClass, null, "executeCommand", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, theOperatingSystemJobsPackage.getJobCapability(), "capability", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, ecorePackage.getEString(), "command", 1, 1, IS_UNIQUE, IS_ORDERED);
		g1 = createEGenericType(ecorePackage.getEMap());
		g2 = createEGenericType(ecorePackage.getEString());
		g1.getETypeArguments().add(g2);
		g2 = createEGenericType(ecorePackage.getEJavaObject());
		g1.getETypeArguments().add(g2);
		addEParameter(op, g1, "variables", 0, 1, IS_UNIQUE, IS_ORDERED);

		op = addEOperation(shellManagerEClass, null, "setDefaultWriter", 0, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, theOperatingSystemJobsPackage.getJobCapability(), "capability", 1, 1, IS_UNIQUE, IS_ORDERED);
		addEParameter(op, ecorePackage.getEString(), "name", 1, 1, IS_UNIQUE, IS_ORDERED);

		// Create resource
		createResource(eNS_URI);
	}

} // CommunicationShellPackageImpl
