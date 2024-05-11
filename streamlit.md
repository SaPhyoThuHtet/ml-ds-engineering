Floating Video

 # Container with expand/collapse button
    button_container = st.container()
    with button_container:
        if st.session_state.show:
            if st.button("⭳", type="primary"):
                st.session_state.show = False
                st.experimental_rerun()
        else:
            if st.button("⭱", type="secondary"):
                st.session_state.show = True
                st.experimental_rerun()

    # Alter CSS based on expand/collapse state
    if st.session_state.show:
        vid_y_pos = "2rem"
        button_css = float_css_helper(width="2.2rem", right="2rem", bottom="21rem", transition=0)
    else:
        vid_y_pos = "-19.5rem"
        button_css = float_css_helper(width="2.2rem", right="2rem", bottom="1rem", transition=0)

    # Float button container
    button_container.float(button_css)

    float_box('<iframe width="100%" height="100%" src="https://www.youtube.com/embed/dQv3t5VCc3U?si=EOu6oaZ35VXqZYsO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>',width="29rem", right="2rem", bottom=vid_y_pos, css="padding: 0;transition-property: all;transition-duration: .5s;transition-timing-function: cubic-bezier(0, 1, 0.5, 1);", shadow=12)

