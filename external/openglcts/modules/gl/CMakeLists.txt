# GL-CTS.es2

set(GLCTS_GL_SRCS
	gl3cClipDistance.cpp
	gl3cClipDistance.hpp
	gl3cCommonBugsTests.cpp
	gl3cCommonBugsTests.hpp
	gl3cTestPackages.cpp
	gl3cTestPackages.hpp
	gl3cCullDistanceTests.cpp
	gl3cCullDistanceTests.hpp
	gl3cGPUShader5Tests.cpp
	gl3cGPUShader5Tests.hpp
	gl3cGLSLnoperspectiveTests.cpp
	gl3cGLSLnoperspectiveTests.hpp
	gl3cTextureSizePromotion.cpp
	gl3cTextureSizePromotion.hpp
	gl3cTextureSwizzleTests.cpp
	gl3cTextureSwizzleTests.hpp
	gl3cTransformFeedbackTests.cpp
	gl3cTransformFeedbackTests.hpp
	gl3cTransformFeedbackOverflowQueryTests.cpp
	gl3cTransformFeedbackOverflowQueryTests.hpp
	gl4cTestPackages.cpp
	gl4cTestPackages.hpp
	gl4cBufferStorageTests.cpp
	gl4cBufferStorageTests.hpp
#	gl4cContextFlushControlTests.cpp
#	gl4cContextFlushControlTests.hpp
	gl4cCopyImageTests.cpp
	gl4cCopyImageTests.hpp
	gl4cDirectStateAccessBuffersTests.cpp
	gl4cDirectStateAccessFramebuffersAndRenderbuffersTests.cpp
	gl4cDirectStateAccessQueriesTests.cpp
	gl4cDirectStateAccessProgramPipelinesTests.cpp
	gl4cDirectStateAccessSamplersTests.cpp
	gl4cDirectStateAccessVertexArraysTests.cpp
	gl4cDirectStateAccessXFBTests.cpp
	gl4cDirectStateAccessTexturesTests.cpp
	gl4cDirectStateAccessTests.cpp
	gl4cDirectStateAccessTests.hpp
	gl4cEnhancedLayoutsTests.cpp
	gl4cEnhancedLayoutsTests.hpp
	gl4cGetTextureSubImageTests.cpp
	gl4cGetTextureSubImageTests.hpp
	gl4cES31CompatibilitySampleVariablesTests.cpp
	gl4cES31CompatibilityShaderImageLoadStoreTests.cpp
	gl4cES31CompatibilityShaderStorageBufferObjectTests.cpp
	gl4cES31CompatibilityTests.cpp
	gl4cES31CompatibilityTests.hpp
	gl4cKHRDebugTests.cpp
	gl4cKHRDebugTests.hpp
	gl4cMapBufferAlignmentTests.cpp
	gl4cMapBufferAlignmentTests.hpp
	gl4cMultiBindTests.cpp
	gl4cMultiBindTests.hpp
	gl4cRobustnessTests.cpp
	gl4cRobustnessTests.hpp
	gl4cShaderAtomicCountersTests.cpp
	gl4cShaderAtomicCountersTests.hpp
	gl4cTextureGatherTests.hpp
	gl4cTextureGatherTests.cpp
	gl4cProgramInterfaceQueryTests.hpp
	gl4cProgramInterfaceQueryTests.cpp
	gl4cComputeShaderTests.cpp
	gl4cComputeShaderTests.hpp
	gl4cConditionalRenderInvertedTests.cpp
	gl4cConditionalRenderInvertedTests.hpp
	gl4cGPUShaderFP64Tests.cpp
	gl4cGPUShaderFP64Tests.hpp
	gl4cIncompleteTextureAccessTests.cpp
	gl4cIncompleteTextureAccessTests.hpp
	gl4cShaderStorageBufferObjectTests.cpp
	gl4cShaderStorageBufferObjectTests.hpp
	gl4cShaderSubroutineTests.cpp
	gl4cShaderSubroutineTests.hpp
	gl4cShaderImageLoadStoreTests.cpp
	gl4cShaderImageLoadStoreTests.hpp
	gl4cShadingLanguage420PackTests.cpp
	gl4cShadingLanguage420PackTests.hpp
	gl4cStencilTexturingTests.cpp
	gl4cStencilTexturingTests.hpp
	gl4cVertexAttrib64BitTest.cpp
	gl4cVertexAttrib64BitTest.hpp
	gl4cVertexAttribBindingTests.cpp
	gl4cVertexAttribBindingTests.hpp
	gl4cShaderImageSizeTests.hpp
	gl4cShaderImageSizeTests.cpp
	gl4cSyncTests.cpp
	gl4cSyncTests.hpp
	gl4cTextureFilterMinmaxTests.cpp
	gl4cTextureFilterMinmaxTests.hpp
	gl4cTextureViewTests.cpp
	gl4cTextureViewTests.hpp
	gl4cTextureBarrierTests.cpp
	gl4cTextureBarrierTests.hpp
	gl4cClipControlTests.cpp
	gl4cClipControlTests.hpp
	gl4cShaderTextureImageSamplesTests.cpp
	gl4cShaderTextureImageSamplesTests.hpp
	gl4cPipelineStatisticsQueryTests.cpp
	gl4cPipelineStatisticsQueryTests.hpp
	gl4cSparseBufferTests.cpp
	gl4cSparseBufferTests.hpp
	gl4cSparseTextureTests.cpp
	gl4cSparseTextureTests.hpp
	gl4cSparseTexture2Tests.cpp
	gl4cSparseTexture2Tests.hpp
	gl4cParallelShaderCompileTests.cpp
	gl4cParallelShaderCompileTests.hpp
	gl4cPostDepthCoverageTests.cpp
	gl4cPostDepthCoverageTests.hpp
	)

set(GLCTS_GL_LIBS
	glcts-common
	glutil
	tcutil
	)

if (DEQP_GTF_AVAILABLE)
	list(APPEND GLCTS_GL_LIBS glcts-gtf)
endif ()

add_library(glcts-gl STATIC ${GLCTS_GL_SRCS})
target_link_libraries(glcts-gl ${GLCTS_GL_LIBS})
