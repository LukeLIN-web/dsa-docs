ADG File Example
=================


The following is an example of an ADG File that is a 2 x 2 Mesh, with 2 input ports and 2 output ports. The processing elements all only have one operation, and the data engines are connected to every port:

.. code-block:: json

    {
    "DSAGenNodes" : {
        "ProcessingElement.0" : {
        "ConfigBitEncode" : {
            "Enabled" : [ 0, 0 ],
            "Instruction_0_Valid" : [ 1, 1 ],
            "Instruction_0_OperandSel_0" : [ 4, 2 ],
            "Instruction_0_OperandSel_1" : [ 7, 5 ],
            "Instruction_0_CtrlMode" : [ 9, 8 ],
            "Instruction_0_CtrlInputSel" : [ 12, 10 ],
            "Instruction_0_Opcode" : [ 16, 13 ],
            "Instruction_0_ResultOut_0" : [ 17, 17 ],
            "Instruction_0_ResultReg_0" : [ 18, 18 ],
            "Instruction_0_Latency" : [ 21, 19 ],
            "MetaCtrlEntry_0_valid" : [ 22, 22 ],
            "MetaCtrlEntry_0_reuseOperand" : [ 24, 23 ],
            "MetaCtrlEntry_0_discardResult" : [ 25, 25 ],
            "MetaCtrlEntry_0_resetReg" : [ 26, 26 ],
            "MetaCtrlEntry_0_abstain" : [ 27, 27 ],
            "MetaCtrlEntry_1_valid" : [ 28, 28 ],
            "MetaCtrlEntry_1_reuseOperand" : [ 30, 29 ],
            "MetaCtrlEntry_1_discardResult" : [ 31, 31 ],
            "MetaCtrlEntry_1_resetReg" : [ 32, 32 ],
            "MetaCtrlEntry_1_abstain" : [ 33, 33 ],
            "MetaCtrlEntry_2_valid" : [ 34, 34 ],
            "MetaCtrlEntry_2_reuseOperand" : [ 36, 35 ],
            "MetaCtrlEntry_2_discardResult" : [ 37, 37 ],
            "MetaCtrlEntry_2_resetReg" : [ 38, 38 ],
            "MetaCtrlEntry_2_abstain" : [ 39, 39 ],
            "MetaCtrlEntry_3_valid" : [ 40, 40 ],
            "MetaCtrlEntry_3_reuseOperand" : [ 42, 41 ],
            "MetaCtrlEntry_3_discardResult" : [ 43, 43 ],
            "MetaCtrlEntry_3_resetReg" : [ 44, 44 ],
            "MetaCtrlEntry_3_abstain" : [ 45, 45 ]
        },
        "dsagen2.comp.config.CompKeys$CompNode$" : {
            "compBits" : 64,
            "comment" : "row0_col0",
            "parameterClassName" : "dsagen2.comp.config.CompNodeParameters",
            "compUnitBits" : 64,
            "nodeType" : "ProcessingElement",
            "nodeId" : 0,
            "supportNodeActive" : true
        },
        "dsagen2.comp.config.CompKeys$OutputBuffer$" : {
            "outputBufferDepth" : 4,
            "parameterClassName" : "dsagen2.comp.config.common.CompNodeOutputBufferParameters",
            "staticOutputBuffer" : false
        },
        "dsagen2.comp.config.CompKeys$RegFile$" : {
            "numReg" : 1,
            "asyncRF" : true,
            "update" : true,
            "parameterClassName" : "dsagen2.comp.config.processing_element.PERegFileParameters",
            "resetRegIdx" : [ 0 ]
        },
        "dsagen2.comp.config.CompKeys$MetaControl$" : {
            "outputLSBCtrl" : true,
            "sizeLUT" : 4,
            "abstain" : true,
            "parameterClassName" : "dsagen2.comp.config.processing_element.PEMetaCtrlParameters",
            "inputLSBCtrl" : true,
            "reuseOperand" : true,
            "resetRegister" : true,
            "discardResult" : true
        },
        "dsagen2.comp.config.CompKeys$DsaOperations$" : {
            "isDynamic" : true,
            "OperationDataTypeSet" : [ "Copy", "Add_I64", "FAdd_D64", "FMul_D64", "FSub_D64", "Max_I64", "Min_I64", "Mul_I64", "Sub_I64" ],
            "maxInstRepeatTime" : 0,
            "definedLatency" : 0,
            "parameterClassName" : "dsagen2.comp.config.processing_element.PEDsaOperationParameters",
            "instSlotSize" : 1,
            "maxFifoDepth" : 4
        }
        },
        "Switch.3" : {
        "ConfigBitEncode" : {
            "Enabled" : [ 0, 0 ],
            "SwitchRouting$_0_SubNet_0" : [ 3, 1 ],
            "SwitchRouting$_1_SubNet_0" : [ 6, 4 ],
            "SwitchRouting$_2_SubNet_0" : [ 9, 7 ],
            "SwitchRouting$_3_SubNet_0" : [ 12, 10 ]
        },
        "dsagen2.comp.config.CompKeys$CompNode$" : {
            "compBits" : 64,
            "comment" : "row1_col1",
            "parameterClassName" : "dsagen2.comp.config.CompNodeParameters",
            "compUnitBits" : 64,
            "nodeType" : "Switch",
            "nodeId" : 3,
            "supportNodeActive" : true
        },
        "dsagen2.comp.config.CompKeys$OutputBuffer$" : {
            "outputBufferDepth" : 4,
            "parameterClassName" : "dsagen2.comp.config.common.CompNodeOutputBufferParameters",
            "staticOutputBuffer" : false
        },
        "dsagen2.comp.config.CompKeys$SwitchRouting$" : {
            "initFullMatrix" : [ ],
            "parameterClassName" : "dsagen2.comp.config.switch.SWRoutingParameters",
            "initIndividualMatrix" : [ ]
        }
        },
        "Switch.2" : {
        "ConfigBitEncode" : {
            "Enabled" : [ 0, 0 ],
            "SwitchRouting$_0_SubNet_0" : [ 2, 1 ],
            "SwitchRouting$_1_SubNet_0" : [ 4, 3 ],
            "SwitchRouting$_2_SubNet_0" : [ 6, 5 ],
            "SwitchRouting$_3_SubNet_0" : [ 8, 7 ]
        },
        "dsagen2.comp.config.CompKeys$CompNode$" : {
            "compBits" : 64,
            "comment" : "row1_col0",
            "parameterClassName" : "dsagen2.comp.config.CompNodeParameters",
            "compUnitBits" : 64,
            "nodeType" : "Switch",
            "nodeId" : 2,
            "supportNodeActive" : true
        },
        "dsagen2.comp.config.CompKeys$OutputBuffer$" : {
            "outputBufferDepth" : 4,
            "parameterClassName" : "dsagen2.comp.config.common.CompNodeOutputBufferParameters",
            "staticOutputBuffer" : false
        },
        "dsagen2.comp.config.CompKeys$SwitchRouting$" : {
            "initFullMatrix" : [ ],
            "parameterClassName" : "dsagen2.comp.config.switch.SWRoutingParameters",
            "initIndividualMatrix" : [ ]
        }
        },
        "Switch.1" : {
        "ConfigBitEncode" : {
            "Enabled" : [ 0, 0 ],
            "SwitchRouting$_0_SubNet_0" : [ 2, 1 ],
            "SwitchRouting$_1_SubNet_0" : [ 4, 3 ],
            "SwitchRouting$_2_SubNet_0" : [ 6, 5 ],
            "SwitchRouting$_3_SubNet_0" : [ 8, 7 ]
        },
        "dsagen2.comp.config.CompKeys$CompNode$" : {
            "compBits" : 64,
            "comment" : "row0_col1",
            "parameterClassName" : "dsagen2.comp.config.CompNodeParameters",
            "compUnitBits" : 64,
            "nodeType" : "Switch",
            "nodeId" : 1,
            "supportNodeActive" : true
        },
        "dsagen2.comp.config.CompKeys$OutputBuffer$" : {
            "outputBufferDepth" : 4,
            "parameterClassName" : "dsagen2.comp.config.common.CompNodeOutputBufferParameters",
            "staticOutputBuffer" : false
        },
        "dsagen2.comp.config.CompKeys$SwitchRouting$" : {
            "initFullMatrix" : [ ],
            "parameterClassName" : "dsagen2.comp.config.switch.SWRoutingParameters",
            "initIndividualMatrix" : [ ]
        }
        },
        "Switch.0" : {
        "ConfigBitEncode" : {
            "Enabled" : [ 0, 0 ],
            "SwitchRouting$_0_SubNet_0" : [ 2, 1 ],
            "SwitchRouting$_1_SubNet_0" : [ 4, 3 ],
            "SwitchRouting$_2_SubNet_0" : [ 6, 5 ],
            "SwitchRouting$_3_SubNet_0" : [ 8, 7 ]
        },
        "dsagen2.comp.config.CompKeys$CompNode$" : {
            "compBits" : 64,
            "comment" : "row0_col0",
            "parameterClassName" : "dsagen2.comp.config.CompNodeParameters",
            "compUnitBits" : 64,
            "nodeType" : "Switch",
            "nodeId" : 0,
            "supportNodeActive" : true
        },
        "dsagen2.comp.config.CompKeys$OutputBuffer$" : {
            "outputBufferDepth" : 4,
            "parameterClassName" : "dsagen2.comp.config.common.CompNodeOutputBufferParameters",
            "staticOutputBuffer" : false
        },
        "dsagen2.comp.config.CompKeys$SwitchRouting$" : {
            "initFullMatrix" : [ ],
            "parameterClassName" : "dsagen2.comp.config.switch.SWRoutingParameters",
            "initIndividualMatrix" : [ ]
        }
        },
        "RecurrenceEngine.0" : {
        "dsagen2.mem.config.MemKeys$MemNode$" : {
            "numWrite" : 1,
            "memUnitBits" : 8,
            "numRead" : 1,
            "MaxLength1D" : 2147483646,
            "parameterClassName" : "dsagen2.mem.config.MemNodeParameters",
            "MaxLength3D" : 0,
            "capacity" : 16384,
            "LinearLength1DStream" : false,
            "numGenDataType" : 0,
            "LinearPadding" : true,
            "MaxAbsStretch3D2D" : 0,
            "NumLength1DUnitBitsExp" : 0,
            "MaxAbsStride3D" : 0,
            "MaxAbsStride1D" : 1,
            "IndirectStride2DStream" : false,
            "AtomicOperations" : [ ],
            "NumIdxUnitBitsExp" : 0,
            "MaxAbsDeltaStride2D" : 0,
            "LinearStride2DStream" : false,
            "MaxLength2D" : 0,
            "MaxAbsStretch2D" : 0,
            "nodeType" : "RecurrenceEngine",
            "supportBuffet" : false,
            "numMemUnitBitsExp" : 4,
            "MaxAbsStretch3D1D" : 0,
            "IndirectIndexStream" : false,
            "NumStride2DUnitBitsExp" : 0,
            "writeWidth" : 32,
            "MaxAbsStride2D" : 0,
            "numPendingRequest" : 0,
            "readWidth" : 32,
            "nodeId" : 0,
            "streamStated" : true,
            "numSpmBank" : 0,
            "IndirectLength1DStream" : false,
            "MaxAbsDeltaStretch2D" : 0
        }
        },
        "RegisterEngine.0" : {
        "dsagen2.mem.config.MemKeys$MemNode$" : {
            "numWrite" : 1,
            "memUnitBits" : 8,
            "numRead" : 1,
            "MaxLength1D" : 0,
            "parameterClassName" : "dsagen2.mem.config.MemNodeParameters",
            "MaxLength3D" : 0,
            "capacity" : 16384,
            "LinearLength1DStream" : false,
            "numGenDataType" : 0,
            "LinearPadding" : false,
            "MaxAbsStretch3D2D" : 0,
            "NumLength1DUnitBitsExp" : 0,
            "MaxAbsStride3D" : 0,
            "MaxAbsStride1D" : 0,
            "IndirectStride2DStream" : false,
            "AtomicOperations" : [ ],
            "NumIdxUnitBitsExp" : 0,
            "MaxAbsDeltaStride2D" : 0,
            "LinearStride2DStream" : false,
            "MaxLength2D" : 0,
            "MaxAbsStretch2D" : 0,
            "nodeType" : "RegisterEngine",
            "supportBuffet" : false,
            "numMemUnitBitsExp" : 4,
            "MaxAbsStretch3D1D" : 0,
            "IndirectIndexStream" : false,
            "NumStride2DUnitBitsExp" : 0,
            "writeWidth" : 8,
            "MaxAbsStride2D" : 0,
            "numPendingRequest" : 0,
            "readWidth" : 8,
            "nodeId" : 0,
            "streamStated" : true,
            "numSpmBank" : 0,
            "IndirectLength1DStream" : false,
            "MaxAbsDeltaStretch2D" : 0
        }
        },
        "GenerateEngine.0" : {
        "dsagen2.mem.config.MemKeys$MemNode$" : {
            "numWrite" : 0,
            "memUnitBits" : 8,
            "numRead" : 1,
            "MaxLength1D" : 2147483646,
            "parameterClassName" : "dsagen2.mem.config.MemNodeParameters",
            "MaxLength3D" : 0,
            "capacity" : 16384,
            "LinearLength1DStream" : true,
            "numGenDataType" : 4,
            "LinearPadding" : true,
            "MaxAbsStretch3D2D" : 0,
            "NumLength1DUnitBitsExp" : 4,
            "MaxAbsStride3D" : 0,
            "MaxAbsStride1D" : 1,
            "IndirectStride2DStream" : true,
            "AtomicOperations" : [ ],
            "NumIdxUnitBitsExp" : 4,
            "MaxAbsDeltaStride2D" : 0,
            "LinearStride2DStream" : true,
            "MaxLength2D" : 2147483646,
            "MaxAbsStretch2D" : 1073741822,
            "nodeType" : "GenerateEngine",
            "supportBuffet" : false,
            "numMemUnitBitsExp" : 4,
            "MaxAbsStretch3D1D" : 0,
            "IndirectIndexStream" : true,
            "NumStride2DUnitBitsExp" : 4,
            "writeWidth" : 0,
            "MaxAbsStride2D" : 1073741822,
            "numPendingRequest" : 16,
            "readWidth" : 8,
            "nodeId" : 0,
            "streamStated" : true,
            "numSpmBank" : 0,
            "IndirectLength1DStream" : true,
            "MaxAbsDeltaStretch2D" : 0
        }
        },
        "ScratchpadMemory.0" : {
        "dsagen2.mem.config.MemKeys$MemNode$" : {
            "numWrite" : 1,
            "memUnitBits" : 8,
            "numRead" : 1,
            "MaxLength1D" : 2147483646,
            "parameterClassName" : "dsagen2.mem.config.MemNodeParameters",
            "MaxLength3D" : 0,
            "capacity" : 524288,
            "LinearLength1DStream" : true,
            "numGenDataType" : 0,
            "LinearPadding" : true,
            "MaxAbsStretch3D2D" : 0,
            "NumLength1DUnitBitsExp" : 4,
            "MaxAbsStride3D" : 0,
            "MaxAbsStride1D" : 1,
            "IndirectStride2DStream" : true,
            "AtomicOperations" : [ ],
            "NumIdxUnitBitsExp" : 4,
            "MaxAbsDeltaStride2D" : 0,
            "LinearStride2DStream" : true,
            "MaxLength2D" : 2147483646,
            "MaxAbsStretch2D" : 1073741822,
            "nodeType" : "ScratchpadMemory",
            "supportBuffet" : false,
            "numMemUnitBitsExp" : 4,
            "MaxAbsStretch3D1D" : 0,
            "IndirectIndexStream" : true,
            "NumStride2DUnitBitsExp" : 4,
            "writeWidth" : 32,
            "MaxAbsStride2D" : 1073741822,
            "numPendingRequest" : 16,
            "readWidth" : 32,
            "nodeId" : 0,
            "streamStated" : true,
            "numSpmBank" : 4,
            "IndirectLength1DStream" : true,
            "MaxAbsDeltaStretch2D" : 0
        }
        },
        "DirectMemoryAccess.0" : {
        "dsagen2.mem.config.MemKeys$MemNode$" : {
            "numWrite" : 1,
            "memUnitBits" : 8,
            "numRead" : 1,
            "MaxLength1D" : 2147483646,
            "parameterClassName" : "dsagen2.mem.config.MemNodeParameters",
            "MaxLength3D" : 0,
            "capacity" : 1099511627776,
            "LinearLength1DStream" : true,
            "numGenDataType" : 0,
            "LinearPadding" : true,
            "MaxAbsStretch3D2D" : 0,
            "NumLength1DUnitBitsExp" : 4,
            "MaxAbsStride3D" : 0,
            "MaxAbsStride1D" : 1,
            "IndirectStride2DStream" : true,
            "AtomicOperations" : [ "Add", "Sub", "Min", "Max" ],
            "NumIdxUnitBitsExp" : 4,
            "MaxAbsDeltaStride2D" : 0,
            "LinearStride2DStream" : true,
            "MaxLength2D" : 2147483646,
            "MaxAbsStretch2D" : 1073741822,
            "nodeType" : "DirectMemoryAccess",
            "supportBuffet" : false,
            "numMemUnitBitsExp" : 4,
            "MaxAbsStretch3D1D" : 0,
            "IndirectIndexStream" : true,
            "NumStride2DUnitBitsExp" : 4,
            "writeWidth" : 32,
            "MaxAbsStride2D" : 1073741822,
            "numPendingRequest" : 16,
            "readWidth" : 32,
            "nodeId" : 0,
            "streamStated" : true,
            "numSpmBank" : 0,
            "IndirectLength1DStream" : true,
            "MaxAbsDeltaStretch2D" : 0
        }
        },
        "InputVectorPort.1" : {
        "dsagen2.sync.config.SyncKeys$IVPNode$" : {
            "vpImpl" : 0,
            "vpStated" : true,
            "parameterClassName" : "dsagen2.sync.config.IVPNodeParameters",
            "depthByte" : 2,
            "nodeType" : "InputVectorPort",
            "repeatedIVP" : true,
            "nodeId" : 1,
            "broadcastIVP" : true
        }
        },
        "InputVectorPort.0" : {
        "dsagen2.sync.config.SyncKeys$IVPNode$" : {
            "vpImpl" : 0,
            "vpStated" : true,
            "parameterClassName" : "dsagen2.sync.config.IVPNodeParameters",
            "depthByte" : 2,
            "nodeType" : "InputVectorPort",
            "repeatedIVP" : true,
            "nodeId" : 0,
            "broadcastIVP" : true
        }
        },
        "OutputVectorPort.1" : {
        "dsagen2.sync.config.SyncKeys$OVPNode$" : {
            "vpImpl" : 0,
            "discardOVP" : true,
            "vpStated" : true,
            "parameterClassName" : "dsagen2.sync.config.OVPNodeParameters",
            "taskOVP" : true,
            "depthByte" : 2,
            "nodeType" : "OutputVectorPort",
            "nodeId" : 1
        }
        },
        "OutputVectorPort.0" : {
        "dsagen2.sync.config.SyncKeys$OVPNode$" : {
            "vpImpl" : 0,
            "discardOVP" : true,
            "vpStated" : true,
            "parameterClassName" : "dsagen2.sync.config.OVPNodeParameters",
            "taskOVP" : true,
            "depthByte" : 2,
            "nodeType" : "OutputVectorPort",
            "nodeId" : 0
        }
        }
    },
    "DSAGenEdges" : [ {
        "SourceNodeType" : "DirectMemoryAccess",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "InputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "DirectMemoryAccess",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 1,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "DirectMemoryAccess",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "ScratchpadMemory",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "ScratchpadMemory",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 0,
        "SinkNodeType" : "DirectMemoryAccess",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "InputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 1,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 2,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "ScratchpadMemory",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "GenerateEngine",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 2,
        "SinkNodeType" : "GenerateEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 1,
        "SinkNodeType" : "ScratchpadMemory",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 0,
        "SourceIndex" : 2,
        "SinkNodeType" : "ProcessingElement",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "InputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 0,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 2,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "RecurrenceEngine",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 3
    }, {
        "SourceNodeType" : "GenerateEngine",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 3,
        "SinkNodeType" : "RecurrenceEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 2,
        "SinkNodeType" : "GenerateEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 1,
        "SourceIndex" : 0,
        "SinkNodeType" : "ProcessingElement",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "RecurrenceEngine",
        "SourceNodeId" : 0,
        "SourceIndex" : 1,
        "SinkNodeType" : "InputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 3
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 0,
        "SourceIndex" : 4,
        "SinkNodeType" : "RegisterEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 3,
        "SinkNodeType" : "RecurrenceEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 2,
        "SourceIndex" : 0,
        "SinkNodeType" : "ProcessingElement",
        "SinkNodeId" : 0,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "OutputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 4,
        "SinkNodeType" : "RegisterEngine",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 3,
        "SourceIndex" : 0,
        "SinkNodeType" : "ProcessingElement",
        "SinkNodeId" : 0,
        "SinkIndex" : 3
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 2,
        "SourceIndex" : 1,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 3,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 3,
        "SourceIndex" : 1,
        "SinkNodeType" : "OutputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 1,
        "SourceIndex" : 1,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 3,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 2,
        "SourceIndex" : 2,
        "SinkNodeType" : "OutputVectorPort",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 3,
        "SourceIndex" : 2,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 2,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "InputVectorPort",
        "SourceNodeId" : 1,
        "SourceIndex" : 1,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 3,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 1,
        "SourceIndex" : 2,
        "SinkNodeType" : "OutputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 0
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 3,
        "SourceIndex" : 3,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 1,
        "SinkIndex" : 2
    }, {
        "SourceNodeType" : "ProcessingElement",
        "SourceNodeId" : 0,
        "SourceIndex" : 0,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 3,
        "SinkIndex" : 3
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 0,
        "SourceIndex" : 3,
        "SinkNodeType" : "OutputVectorPort",
        "SinkNodeId" : 1,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 1,
        "SourceIndex" : 3,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 0,
        "SinkIndex" : 1
    }, {
        "SourceNodeType" : "Switch",
        "SourceNodeId" : 2,
        "SourceIndex" : 3,
        "SinkNodeType" : "Switch",
        "SinkNodeId" : 0,
        "SinkIndex" : 2
    } ]
    }

Visualized, this adg would look like the following:



.. toctree::
   :maxdepth: 1