---
title: XRRenderState
slug: Web/API/XRRenderState
page-type: web-api-interface
tags:
  - API
  - AR
  - Augmented Reality
  - Interface
  - Reference
  - VR
  - Virtual Reality
  - WebXR
  - WebXR Device API
  - XRRenderState
  - Experimental
browser-compat: api.XRRenderState
---
{{securecontext_header}}{{APIRef("WebXR")}}{{SeeCompatTable}}

The **`XRRenderState`** interface of the [WebXR Device API](/en-US/docs/Web/API/WebXR_Device_API) contains configurable values which affect how the imagery generated by an {{DOMxRef("XRSession")}} gets composited. These properties include the range of distances from the viewer within which content should be rendered, the vertical field of view (for inline presentations), and a reference to the {{domxref("XRWebGLLayer")}} being used as the target for rendering the scene prior to it being presented on the XR device's display or displays.

When you apply changes using the `XRSession` method {{domxref("XRSession.updateRenderState", "updateRenderState()")}}, the specified changes take effect after the current animation frame has completed, but before the next one begins.

## Properties

- {{DOMxRef("XRRenderState.baseLayer")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : The {{DOMxRef("XRWebGLLayer")}} from which the browser's compositing system obtains the image for the XR session.
- {{DOMxRef("XRRenderState.depthFar")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : The distance, in meters, of the **far clip plane** from the viewer. The far clip plane is the plane which is parallel to the display beyond which rendering of the scene no longer takes place. This, essentially, specifies the maximum distance the user can see.
- {{DOMxRef("XRRenderState.depthNear")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : The distance, in meters, of the **near clip plane** from the viewer. The near clip plane is the plane, parallel to the display, at which rendering of the scene begins. Any closer to the viewer than this, and no portions of the scene are drawn.
- {{DOMxRef("XRRenderState.inlineVerticalFieldOfView")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : The default vertical field of view, defined in radians, to use when the session is in `inline` mode. `null` for all immersive sessions.
- {{DOMxRef("XRRenderState.layers")}} {{ReadOnlyInline}}
  - : An ordered array containing {{domxref("XRLayer")}} objects that are displayed by the XR compositor.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{DOMxRef("XRSession.renderState")}}
- {{DOMxRef("XRSession.updateRenderState()")}}
- {{DOMxRef("XRSystem.requestSession", "navigator.xr.requestSession()")}}
