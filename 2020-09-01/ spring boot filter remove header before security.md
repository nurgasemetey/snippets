###  spring boot filter remove header before security


[java - How can we remove &quot;Authorization&quot; Header from a 'HttpServletRequest' - Stack Overflow](https://stackoverflow.com/questions/33612555/how-can-we-remove-authorization-header-from-a-httpservletrequest "java - How can we remove &quot;Authorization&quot; Header from a 'HttpServletRequest' - Stack Overflow")



[rest - How to modify Http headers before executing request in spring boot mvc - Stack Overflow](https://stackoverflow.com/questions/50543520/how-to-modify-http-headers-before-executing-request-in-spring-boot-mvc "rest - How to modify Http headers before executing request in spring boot mvc - Stack Overflow")

[spring - Handle UserRedirectRequiredException (A redirect is required to get the users approval) - Stack Overflow](https://stackoverflow.com/questions/32201870/handle-userredirectrequiredexception-a-redirect-is-required-to-get-the-users-ap/32227901#32227901 "spring - Handle UserRedirectRequiredException (A redirect is required to get the users approval) - Stack Overflow")


 

```
package com.parabol.microservices.metistraffic.filters;

import org.springframework.web.filter.GenericFilterBean;

import javax.servlet.*;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletRequestWrapper;
import java.io.IOException;
import java.util.*;

public class CustomFilter implements Filter {

    public class HeaderMapRequestWrapper extends HttpServletRequestWrapper {
        /**
         * construct a wrapper for this request
         *
         * @param request
         */
        HttpServletRequest request;
        public HeaderMapRequestWrapper(HttpServletRequest request) {
            super(request);
            this.request = request;
        }


        @Override
        public String getHeader(String name) {
            if ("Authorization".equalsIgnoreCase(name)) {
                return null;
            }
            return super.getHeader(name);
        }

        /**
         * get the Header names
         */
        @Override
        public Enumeration<String> getHeaderNames() {
//            if(request.getRequestURI().contains(""))
            List<String> names = Collections.list(super.getHeaderNames());
            names.remove("authorization");
            return Collections.enumeration(names);
        }

        @Override
        public Enumeration<String> getHeaders(String name) {
            System.out.println(request.getRequestURI());
            if ("Authorization".equalsIgnoreCase(name)) {
                return Collections.<String>emptyEnumeration();
            }
            return super.getHeaders(name);
        }

    }

    @Override
    public void init(FilterConfig filterConfig) throws ServletException {

    }

    @Override
    public void doFilter(
      ServletRequest request,
      ServletResponse response,
      FilterChain chain) throws IOException, ServletException {
        HttpServletRequest req = (HttpServletRequest) request;
        HeaderMapRequestWrapper requestWrapper = new HeaderMapRequestWrapper(req);
        chain.doFilter(requestWrapper, response);
    }

    @Override
    public void destroy() {

    }
}

---
    @Override
    public void configure(HttpSecurity http) throws Exception {

        http
                .addFilterBefore(new CustomFilter(), SecurityContextPersistenceFilter.class)

```
