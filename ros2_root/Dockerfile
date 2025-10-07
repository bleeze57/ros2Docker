FROM osrf/ros:humble-desktop
SHELL ["/bin/bash", "-c"]
WORKDIR /app
COPY ros2_ws ros2_root/ros2_ws
RUN cd ros2_root && \
    source /opt/ros/humble/setup.bash && \
    colcon build --packages-select cpp_srvcli
# Copy and fix permissions on the entrypoint
COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
CMD ["bash"]
