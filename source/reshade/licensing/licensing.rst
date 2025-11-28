Software Licensing
==================

This guide provides an overview of software licensing, with a particular focus on its relevance to ReShadeFX shaders. Understanding licensing is crucial for both creators and users to ensure proper usage, distribution, and modification of software.

Purpose of Licenses
-------------------

Software licenses are legal instruments that govern the use and distribution of software. They define the rights and restrictions that apply to a piece of software, protecting the intellectual property of the creator while enabling others to use, share, or modify the work under specified conditions.

Key purposes of software licenses include:

- **Protecting Creator Rights:** Licenses allow creators to retain ownership and control over their work, specifying how it can be used, copied, distributed, and adapted.
- **Granting User Permissions:** They provide users with explicit permissions to interact with the software, such as running it, studying its code, modifying it, or distributing it.
- **Establishing Legal Framework:** Licenses create a clear legal framework, reducing ambiguity and potential disputes regarding software usage.
- **Promoting Collaboration and Innovation:** Open-source licenses, in particular, encourage collaboration by allowing others to build upon existing work, fostering innovation within communities.

Common Open-Source Licenses
---------------------------

Open-source licenses are designed to make source code available for use, modification, and distribution under terms that ensure its openness. They generally fall into two main categories: **permissive** and **copyleft**.

Permissive Licenses
^^^^^^^^^^^^^^^^^^^

These licenses impose minimal restrictions on how the software can be used, modified, and distributed. They often only require attribution.

MIT License [#mit]_
   A very short and simple license that allows users to do almost anything with the software, provided they include the original copyright and license notice. It's highly compatible with other licenses.

Apache License 2.0 [#apache]_
   A permissive license that grants users a patent license, which is useful for preventing patent lawsuits. It also requires attribution and preservation of copyright notices.

BSD Licenses (2-clause and 3-clause) [#bsd]_
   Similar to MIT, these are permissive licenses that primarily require attribution. The 3-clause version adds a clause preventing endorsement of products derived from the software without specific written permission.

Copyleft Licenses
^^^^^^^^^^^^^^^^^

These licenses require that any derivative works also be released under the same or a compatible copyleft license. This ensures that the "freedom" of the software is preserved down the line.

GNU General Public License (GPL) (various versions) [#gpl]_
   A strong copyleft license. If you distribute software that includes GPL-licensed code, your entire software must also be licensed under the GPL. This is often referred to as the "viral" nature of GPL.

GNU Lesser General Public License (LGPL) [#lgpl]_
   A weaker copyleft license than GPL. It allows proprietary software to link to LGPL-licensed libraries without requiring the proprietary software itself to be licensed under LGPL. However, if the LGPL-licensed code is modified, the modifications must be released under LGPL.

Mozilla Public License (MPL) [#mpl]_
   A "file-level" copyleft license. It requires modifications to MPL-licensed files to be released under MPL, but allows other files in the same project to be under different licenses.

License Compatibilities
-----------------------

Understanding license compatibility is crucial when combining code from different sources. Incompatible licenses can create legal issues, preventing the distribution of a combined work.

- **Permissive licenses** are generally highly compatible with each other and with copyleft licenses, as they impose few restrictions. For example, MIT-licensed code can often be incorporated into GPL-licensed projects.
- **Copyleft licenses** have stricter compatibility requirements. For instance, combining GPL-licensed code with code under an incompatible license (even another copyleft license) can be problematic, as the terms of both licenses might conflict regarding how the combined work must be licensed.

When in doubt, it is always best to consult legal counsel or choose components with clearly compatible licenses.

What to Do If There Is No License
---------------------------------

If a piece of software, including a ReShadeFX shader, does not explicitly include a license, it is generally considered to be under **exclusive copyright** by default. This means:

- **No Permissions Granted:** You do not have permission to use, copy, distribute, or modify the software without explicit authorization from the copyright holder.
- **Risk of Infringement:** Using unlicensed software without permission can lead to copyright infringement claims.

Therefore, if you encounter software without a license:

#. **Assume Exclusive Copyright:** Operate under the assumption that you have no rights to use the software beyond what fair use (if applicable) might allow.
#. **Contact the Author:** The best course of action is to contact the author or creator and request clarification on licensing or seek explicit permission for your intended use.
#. **Avoid Use if Unsure:** If you cannot obtain clear licensing information or permission, it is safest to avoid using the software to prevent potential legal issues.

For ReShadeFX shaders, always check for a :file:`LICENSE` file, a :file:`README` section on licensing, or comments within the shader code itself that specify the license. If none are present, reach out to the shader's creator.

References
----------

.. [#apache] Apache License 2.0: http://www.apache.org/licenses/LICENSE-2.0
.. [#bsd] BSD 3-Clause License: https://opensource.org/licenses/BSD-3-Clause
.. [#gpl] GNU General Public License v3: https://www.gnu.org/licenses/gpl-3.0.html
.. [#lgpl] GNU Lesser General Public License v3: https://www.gnu.org/licenses/lgpl-3.0.html
.. [#mit] MIT License: https://opensource.org/licenses/MIT
.. [#mpl] Mozilla Public License 2.0: https://www.mozilla.org/MPL/2.0/

Disclaimer
----------

The authors of this page are not legal professionals. The information provided here is for general informational purposes only and does not constitute legal advice. For specific legal matters, please consult with a qualified legal professional.
