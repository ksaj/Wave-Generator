globals [
  membrane-edge-x  ;; horizontal distance from center to edge of membrane
  membrane-edge-y  ;; vertical distance from center to edge of membrane
]

turtles-own [
  edge?            ;; are we on the edge of the membrane?
  driver?          ;; are we part of the green driving plate?
  x                ;; position on x axis in space
  y                ;; position on y axis in space
  z                ;; position on z axis in space
  velocity         ;; velocity along z axis
  neighbor-turtles ;; agentset of turtles adjacent to us
]

to setup
  clear-all
  set membrane-edge-x floor (max-pxcor / 2)
  set membrane-edge-y floor (max-pycor / 2)
  set-default-shape turtles "circle"
  ask patches with [(abs pxcor <= membrane-edge-x) and
                    (abs pycor <= membrane-edge-y)]
    [ sprout 1
        [ set edge? (abs xcor = membrane-edge-x) or
                    (abs ycor = membrane-edge-y)
          if edge? [ set color blue ]
          set driver? (abs (xcor - driver-x) <= driver-size) and
                      (abs (ycor - driver-y) <= driver-size)
          if driver? [ set color green ]
          set x xcor
          set y ycor
          set z 0
          set velocity 0
          recolor ] ]
  ask turtles
    [ set neighbor-turtles turtles-on neighbors4 ]
  project
  reset-ticks
end

to recolor  ;; turtle procedure
  if not edge? and not driver?
    [ set color scale-color red z -20 20 ]
end

to go
  ask turtles with [not driver? and not edge?]
    [ propagate ]
  ask turtles
    [ ifelse driver?
        [ set z (driver-amplitude * (sin (0.1 * driver-frequency * ticks))) ]
        [ set z (z + velocity)
          recolor ] ]
  project
  tick
end

to propagate   ;; turtle procedure -- propagates the wave from neighboring turtles
  set velocity (velocity +
                 (stiffness * 0.01 *
                   (sum [z] of neighbor-turtles
                    - 4 * z)))
  set velocity (((1000 - friction) / 1000) * velocity)
end

;;; procedures for displaying in 2-D or 3-D

to project
  ifelse three-d?
    [ project-3d ]
    [ project-2d ]
end

to project-3d
  ask turtles [
    let xc (x + (cos view-angle) * y)
    let yc (z + (sin view-angle) * y)
    ifelse patch-at (xc - xcor) (yc - ycor) != nobody
    [ setxy  xc yc
      show-turtle ]
    [ hide-turtle ]
    recolor
  ]
end

to project-2d
  ;; Set our viewable x and y coordinates to be the same as our real
  ;; coordinates.  This is only needed for if the user turns THREE-D?
  ;; off while the model is running.
  ask turtles
    [ setxy x y
      recolor
      show-turtle ]
end


; Copyright 1997 Uri Wilensky.
; See Info tab for full copyright and license.

